# 🎬 Como as apresentações são feitas

As apresentações de cada módulo são escritas em **Markdown** e convertidas em PDF pelo [Marp](https://marp.app/). Nada precisa ser instalado: o `npx` baixa as ferramentas sob demanda e o export usa o Google Chrome que já está na máquina.

Nos outros quatro cursos da trilha cada módulo é uma **pasta**, e a apresentação mora numa subpasta `apresentacao/` dentro dela. Aqui não dá: o material escrito é **um `.md` por módulo na raiz** do repositório, sem pasta por módulo. A adaptação fiel do padrão, então, é uma única pasta `apresentacao/` com todos os decks:

```
curso-vscode/
├── 01-introducao-instalacao.md              # a aula escrita
├── 02-interface.md
├── ...
├── apresentacao/
│   ├── apresentacao-01-introducao-instalacao.md   # a fonte  ← edite este
│   ├── apresentacao-01-introducao-instalacao.pdf  # o gerado ← projete este
│   ├── ...
│   └── img/
│       ├── ciclo-editar-rodar.mmd           # diagrama, versão para projeção
│       ├── ciclo-editar-rodar.svg           # gerado do .mmd
│       ├── source-control.mmd
│       └── source-control.svg
└── recursos/
    └── slides/                              # a infraestrutura (esta pasta)
        ├── trilha.css
        ├── gerar.sh
        ├── marp.config.mjs
        └── conferir.py
```

A infraestrutura fica em `recursos/slides/` como nos outros quatro cursos — assim o comando é o mesmo em toda a trilha.

Cada módulo aponta para o seu PDF logo abaixo do título, com uma linha `> 🎬 **Slides da aula:**`.

**Os dois são versionados.** O `.md` para o `git diff` mostrar o que mudou; o `.pdf` para abrir na aula sem depender de gerar nada na hora.

## Gerar

```bash
bash recursos/slides/gerar.sh              # tudo o que estiver desatualizado
bash recursos/slides/gerar.sh 03-edicao    # só um módulo
bash recursos/slides/gerar.sh --forcar     # regera tudo
bash recursos/slides/gerar.sh --html       # gera .html além do .pdf
```

O script compara datas: só regera o que mudou, e regera todos os decks quando o tema muda.

> ⚠️ O `trilha.css` e o `marp.config.mjs` precisam ficar **ao lado do `gerar.sh`**, nesta pasta. O script resolve os caminhos a partir da própria localização e aborta se não os encontrar — antes ele os procurava num caminho fixo, e mover a pasta quebrava a geração de um jeito silencioso.

> 💡 **Enquanto escreve**, a extensão [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) mostra o preview lado a lado e evita rodar o script a cada ajuste. Para ela enxergar o tema, adicione em `.vscode/settings.json`:
> ```json
> { "markdown.marp.themes": ["./recursos/slides/trilha.css"] }
> ```

## Conferir se algum slide estourou

```bash
python3 recursos/slides/conferir.py             # todos os decks
python3 recursos/slides/conferir.py 03-edicao   # só um
```

**O Marp não avisa quando o conteúdo passa do slide** — ele simplesmente deixa o texto atravessar o rodapé, e o defeito só aparece olhando o PDF. Este script estima a altura de cada slide a partir das métricas do `trilha.css` e marca:

- ❌ acima de 102% da área útil — quase certamente estourando;
- ⚠️ acima de 92% — no limite, vale abrir o PNG e olhar.

É estimativa, não medição: aponta onde olhar, não substitui a conferida visual. Rode antes de fechar cada deck.

> 💡 Regra de bolso que sai das métricas: um bloco de código sozinho com o título cabe até **~11 linhas**; uma tabela de 2 colunas, até **~8 linhas**. Passou disso, divida em dois slides.

## Escrever um deck

`---` separa slides. O cabeçalho vai só no começo do arquivo:

```markdown
---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 1'
---
```

### Classes de slide

Aplicadas com um comentário na primeira linha do slide: `<!-- _class: lead -->`.

| Classe | Para quê |
|---|---|
| `capa` | Primeiro slide. Faixa colorida na lateral, sem número de página |
| `lead` | Uma ideia só, centralizada, fundo tingido — as analogias 💡 |
| `diagrama` | Título no topo e a imagem centrada no espaço restante |
| `checkpoint` | Fechamento do módulo, fundo tingido |
| `lista-limpa` | Lista cujos itens já começam com emoji (tira a bolinha) |
| `tabela-densa` | Tabelas de 7 linhas ou mais |

Pode combinar: `<!-- _class: lead lista-limpa -->`.

### Diagramas

O `.mmd` do slide é **propositalmente diferente** do bloco ` ```mermaid ` do material escrito: o do material é para ler de perto; o do slide precisa de rótulos curtos e traço grosso para sobreviver à projeção.

Ao inserir, **declare a largura** — sem ela o SVG colapsa:

```markdown
![w:900](img/ciclo-editar-rodar.svg)
```

## Armadilhas já resolvidas

Estas custaram tempo. Estão documentadas no CSS, no `gerar.sh` e no `marp.config.mjs`, mas ficam aqui também:

1. **O `marp-cli` lê o stdin como mais um documento** quando ele não é um TTY. Dentro de um `while read` alimentado por `find`, o stdin herdado carrega o caminho do *próximo* deck — o marp conta dois documentos e aborta com *"Output path cannot specify with processing multiple files"*. Daí o `< /dev/null` em toda chamada de `npx` dentro dos laços do `gerar.sh`. **Fica invisível enquanto o repositório tem um único deck**;

2. **`fontFamily` do Mermaid é chave de topo**, não de `themeVariables` — lá dentro é silenciosamente ignorada;

3. **O tema `default` do Marp embute o CSS de Markdown do GitHub**, que traz `section table { display: block; width: max-content }`. Como o Marp prefixa as regras do tema com `section`, um seletor solto (`td` → `section td`) perde para o `section table td` do GitHub. Por isso as regras de tabela já vêm qualificadas com `table`;

4. **Emoji do Marp virava `<img>` de CDN externo.** O `marp.config.mjs` desliga o Twemoji: sem isso, gerar o PDF e exibir o HTML exigiriam internet — e qualquer regra CSS de `img` afetaria emoji;

5. **`:only-child` ignora nós de texto.** Num parágrafo `<img>seguido de texto</p>` a imagem conta como filha única, então uma regra `p > img:only-child` pega o emoji de um callout;

6. **Caminho fixo para o tema quebra ao mover a pasta.** O `gerar.sh` resolve tudo a partir de `BASH_SOURCE` e valida a existência dos arquivos antes de começar.

## Adaptar para outro curso da trilha

Copie a pasta `slides/` inteira e mude **apenas** as duas variáveis no topo do `trilha.css`:

| Curso | `--accent` | `--accent-suave` |
|---|---|---|
| 🔵 VS Code | `#007acc` | `#e6f3fb` |
| 📚 Git e GitHub | `#f05033` | `#fdeeeb` |
| 🟨 JavaScript | `#c9a800` | `#fdf9e3` |
| ☕ Java e POO | `#e76f00` | `#fdf1e6` |
| 🗄️ Modelagem de Dados | `#336791` | `#eaf0f5` |

O `gerar.sh` funciona sem edição — ele varre por `apresentacao-*.md` e `*.mmd` a partir da raiz do repositório, seja qual for a profundidade das pastas.

---

🏠 [Voltar ao início](../../README.md)
