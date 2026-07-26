---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 7'
---

<!-- _class: capa -->

<div class="emoji">⚙️</div>

# Configurações e Produtividade

## Módulo 7 · Curso de VS Code

<div class="meta">Deixar o editor com a sua cara — e o último empurrão de velocidade</div>

---

## Roteiro

1. O sistema de configurações — **User** × **Workspace**
2. As configurações que valem a pena ligar
3. **Emmet** — HTML em alta velocidade
4. **Snippets** — seus próprios atalhos de código
5. **Debugger** — além do `console.log`

---

## Duas formas de configurar

`Ctrl+,` abre as configurações. Há duas visões da mesma coisa:

- **Interface gráfica** — busca e caixinhas. Ótima para **descobrir** o que existe;
- **JSON** — `Ctrl+Shift+P` → *Open User Settings (JSON)*. Ótima para **colar** configurações prontas.

---

## User × Workspace

| Escopo | Onde fica | Vale para |
|---|---|---|
| **User** | seu perfil no sistema | **todos** os seus projetos |
| **Workspace** | `.vscode/settings.json` no projeto | **só aquele projeto** — e vai junto no Git |

> 💡 **Em equipe isso importa:** um `.vscode/settings.json` versionado deixa todo mundo com a mesma formatação, e o diff do Pull Request para de encher de mudança de espaçamento.

---

## As configurações para começar

```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "files.autoSave": "onFocusChange",
  "editor.linkedEditing": true
}
```

Cole no seu `settings.json` e siga em frente — no próximo slide, o que cada uma faz.

---

## O que cada uma faz

| Opção | O que faz |
|---|---|
| `formatOnSave` | formata ao salvar — você viu no Módulo 3 |
| `tabSize: 2` | indentação de 2 espaços; em Java, 4 é o comum |
| `wordWrap` | quebra linhas longas **visualmente**, sem mudar o arquivo |
| `autoSave` | salva ao trocar de janela. Adeus, "esqueci de salvar" |
| `linkedEditing` | em HTML, editar a tag de abertura edita a de fechamento |

---

## Temas e aparência

- **`Ctrl+K Ctrl+T`** — troca o tema de cores;
- **`Ctrl+=` / `Ctrl+-`** — zoom da interface inteira;
- Tamanho da fonte do editor: busque `font size` nas configurações.

> 💡 O zoom de interface é o que salva na hora de **projetar código** — dê dois `Ctrl+=` antes de começar a aula ou a apresentação.

---

## Emmet — HTML e CSS em alta velocidade

Já vem embutido. Digite a abreviação e pressione **`Tab`**:

| Você digita | Vira |
|---|---|
| `!` | a estrutura HTML5 completa |
| `div.card` | `<div class="card"></div>` |
| `ul>li*3` | uma lista com 3 itens |
| `h1{Olá}` | `<h1>Olá</h1>` |
| `.container>.row>.col*2` | estrutura aninhada de divs |

---

## Snippets — seus próprios atalhos

`Ctrl+Shift+P` → **Snippets: Configure Snippets** → escolha a linguagem:

```json
{
  "Console log rápido": {
    "prefix": "cl",
    "body": "console.log($1);",
    "description": "Atalho para console.log"
  }
}
```

Agora `cl` + `Tab` gera `console.log()` com o cursor já **dentro** dos parênteses — é o que o `$1` marca.

---

<!-- _class: lead -->

## 🐞 O `console.log` é útil

O **debugger** é profissional.

Com ele você não adivinha o valor de uma variável:
você **pausa o programa e olha**.

---

## Depurando em três passos

1. Clique na **margem esquerda** de uma linha — nasce um **breakpoint** (bolinha vermelha);
2. **`F5`** — em `.js` escolha *Node.js*; em Java a extensão já cuida;
3. A execução **pausa** ali. Agora:

| Tecla | Ação |
|---|---|
| `F10` | executa a próxima linha (*step over*) |
| `F11` | **entra** dentro da função (*step into*) |
| `F5` | continua até o próximo breakpoint |

---

<!-- _class: lista-limpa -->

## Dicas finais

- ⌨️ **`Ctrl+K Ctrl+S`** — a lista de **todos** os atalhos, e onde você personaliza os seus;
- ↩️ **`Ctrl+Shift+T`** — reabre a aba fechada, igual ao navegador;
- 🎭 **Perfis** — conjuntos de extensões e configurações por contexto;
- ☁️ **Settings Sync** — leva tudo para outra máquina pela conta do GitHub.

> ⚠️ Não ative o Settings Sync em computador compartilhado.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Configurei o `settings.json` com as opções recomendadas;
- ☐ Testei o Emmet em um arquivo HTML;
- ☐ Criei um snippet próprio;
- ☐ Executei um programa com breakpoint e inspecionei variáveis.

---

<!-- _class: lead -->

## 🎓 Fim do curso

Você domina o essencial do VS Code.

**1.** Use os atalhos até virarem automáticos — o `CHEATSHEET.md` ajuda
**2.** Na dúvida, abra a paleta: quase tudo está lá
**3.** Deu errado? `TROUBLESHOOTING.md`

O editor só fica rápido com o uso. Comece hoje.
