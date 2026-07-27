---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 2'
---

<!-- _class: capa -->

<div class="emoji">🗺️</div>

# Conhecendo a Interface

## Módulo 2 · Curso de VS Code

<div class="meta">As seis regiões da janela — e o atalho que abre tudo</div>

---

## Roteiro

1. As **seis regiões** da janela
2. Barra de atividades e Explorer
3. O editor: abas, preview, minimapa
4. **A paleta de comandos** — o recurso mais importante
5. Painel inferior e barra de status

---

## A janela em seis regiões

```
┌──┬───────────┬─────────────────────────────────┐
│A │           │  Abas dos arquivos abertos      │
│T │  BARRA    │ ┌─────────────────────────────┐ │
│I │  LATERAL  │ │                             │ │
│V │           │ │          EDITOR             │ │
│I │ Explorer  │ │  (onde você escreve código) │ │
│D │ Busca     │ ├─────────────────────────────┤ │
│A │ Git       │ │  PAINEL (Terminal, Saída)   │ │
│D │ Extensões │ └─────────────────────────────┘ │
│E ├───────────┴─────────────────────────────────┤
│S │  BARRA DE STATUS (branch, linguagem)        │
└──┴─────────────────────────────────────────────┘
```

---

<!-- _class: tabela-densa -->

## Barra de atividades — a coluna de ícones

| Ícone | Nome | Atalho | Para quê |
|---|---|---|---|
| 📄 | **Explorer** | `Ctrl+Shift+E` | árvore de arquivos |
| 🔍 | **Search** | `Ctrl+Shift+F` | buscar em **todos** os arquivos |
| 🔀 | **Source Control** | `Ctrl+Shift+G` | Git integrado — Módulo 6 |
| 🐞 | **Run and Debug** | `Ctrl+Shift+D` | executar e depurar |
| 🧩 | **Extensions** | `Ctrl+Shift+X` | instalar extensões — Módulo 4 |

> 💡 `Ctrl+B` esconde e mostra a barra lateral — espaço de tela na hora que você precisa.

---

## Explorer — a árvore do projeto

- **Novo arquivo / pasta:** botões no topo, ou clique direito;
- **Renomear:** `F2` · **Excluir:** `Delete`;
- **Mover:** arrastar e soltar.

> 💡 **Truque que economiza cliques:** ao criar um arquivo, digite o caminho inteiro — `src/utils/ajuda.js`. O VS Code cria as pastas `src` e `utils` sozinho.

---

<!-- _class: lista-limpa -->

## As cores ao lado dos arquivos

Quando o projeto usa Git, o Explorer avisa o estado de cada arquivo:

- 🟢 **Verde + U** — *untracked*, arquivo novo, ainda não rastreado;
- 🟡 **Amarelo + M** — *modified*, mudou desde o último commit;
- ⚫ **Ponto ● na aba** — há alterações **não salvas**.

---

## O editor: abas e divisão de tela

| Atalho | Ação |
|---|---|
| `Ctrl+Tab` | alterna entre abas abertas |
| `Ctrl+W` | fecha a aba atual |
| `Ctrl+\` | **divide a tela** — ótimo para comparar dois arquivos |
| `Ctrl+Shift+T` | reabre a última aba fechada |

---

## Modo preview: por que a aba some?

Clicar **uma vez** num arquivo abre em *modo preview* — o nome fica em **itálico** na aba. Clicar em outro arquivo **substitui** essa aba.

Para fixar de vez:

- **duplo clique** no arquivo, ou
- **duplo clique** na própria aba, ou
- simplesmente comece a editar.

> 💡 Não é bug: é o editor evitando encher a barra de abas enquanto você só navega pelo projeto.

---

<!-- _class: lista-limpa -->

## Dois auxiliares que ficam em volta do código

- 🗺️ **Minimapa** — a coluna estreita à **direita**: o arquivo inteiro em miniatura. Ajuda em arquivo longo; some em `View → Appearance → Minimap`;
- 🍞 **Breadcrumbs** — a trilha **acima** do código: `src > utils > ajuda.js > minhaFuncao`. Clicar em cada parte navega pela estrutura.

> 💡 Os dois respondem à mesma pergunta: **onde eu estou neste arquivo?**

---

<!-- _class: lead -->

## Se você decorar um único atalho

# `Ctrl+Shift+P`

A **paleta de comandos** dá acesso a **tudo** que o VS Code faz — sem decorar menu nenhum.

---

## O que dá para fazer pela paleta

Basta digitar o que você quer:

| Digite | E ela abre |
|---|---|
| `settings` | as configurações |
| `theme` | a troca de tema de cores |
| `terminal` | o terminal integrado |
| `format` | a formatação do documento |

> 💡 A busca é **aproximada**: digitar `fmt doc` já encontra *Format Document*.

---

## A prima da paleta: Quick Open

`Ctrl+P` — **sem Shift** — busca **arquivos** pelo nome.

| Digite | E vai para |
|---|---|
| `ajuda` | o arquivo `src/utils/ajuda.js` |
| `:25` | a linha 25 do arquivo atual |
| `@` | a lista de funções e classes do arquivo |
| `?` | tudo o que o Quick Open sabe fazer |

**`Ctrl+P`** busca arquivos · **`Ctrl+Shift+P`** busca comandos.

---

## Painel inferior — `Ctrl+J`

| Guia | Para quê |
|---|---|
| **Problems** | erros e avisos do código — clique e vá até a linha |
| **Output** | mensagens das ferramentas e extensões |
| **Debug Console** | saída durante a depuração |
| **Terminal** | o terminal integrado — Módulo 5 |

---

<!-- _class: lista-limpa -->

## Barra de status — o rodapé que informa

Da esquerda para a direita:

- 🔀 **Branch do Git** — clicar permite **trocar de branch**;
- ⚠️ Contagem de **erros e avisos**;
- 📍 **Linha e coluna** do cursor;
- 🔤 **Codificação** do arquivo — UTF-8;
- 🧠 **Linguagem** detectada — clicar permite mudar.

> ⚠️ Código sem cor? Confira aqui se a linguagem foi detectada certa.

---

## Modo Zen e tela cheia

- **`F11`** — tela cheia;
- **`Ctrl+K Z`** — **Modo Zen**: esconde tudo, deixa só o código. `Esc Esc` para sair.

> 💡 O Modo Zen é ótimo para projetar código em aula ou apresentação — some com toda a distração da interface.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Sei alternar entre Explorer, Busca, Git e Extensões;
- ☐ Sei abrir a paleta de comandos — `Ctrl+Shift+P`;
- ☐ Sei buscar arquivos pelo nome — `Ctrl+P`;
- ☐ Sei abrir o painel e o terminal — `Ctrl+J`;
- ☐ Identifico a branch do Git na barra de status.

---

<!-- _class: lead -->

## ➡️ Próximo passo

**Módulo 3 — Edição Produtiva**

Escrever e modificar código mais rápido,
tirando as mãos do mouse.
