# Módulo 2 — Conhecendo a Interface

[← Módulo anterior](01-introducao-instalacao.md) | [Voltar ao índice](README.md) | [Próximo módulo →](03-edicao-produtiva.md)

---

## 2.1 Visão geral

A janela do VS Code é dividida em **6 regiões principais**:

```
┌─┬──────────────────────────────────────────────┐
│A│  Abas dos arquivos abertos                   │
│t│ ┌──────────────────────────────────────────┐ │
│i│ │                                          │ │
│v│ │                                          │ │
│i│ │            EDITOR                        │ │
│d│ │       (onde você escreve código)         │ │
│a│ │                                          │ │
│d│ ├──────────────────────────────────────────┤ │
│e│ │  PAINEL (Terminal, Problemas, Saída...)  │ │
│s│ └──────────────────────────────────────────┘ │
├─┴──────────────────────────────────────────────┤
│  BARRA DE STATUS (branch git, linguagem, etc.) │
└────────────────────────────────────────────────┘
   ↑
   Barra Lateral (Explorer, Busca, Git, Extensões...)
```

Vamos conhecer cada parte.

---

## 2.2 Barra de Atividades (Activity Bar)

É a coluna de ícones na **extrema esquerda**. Cada ícone abre uma "visão" diferente na barra lateral:

| Ícone | Nome | Atalho | Para quê |
|-------|------|--------|----------|
| 📄 | **Explorer** | `Ctrl+Shift+E` | Árvore de arquivos do projeto |
| 🔍 | **Search** | `Ctrl+Shift+F` | Buscar texto em **todos** os arquivos |
| 🔀 | **Source Control** | `Ctrl+Shift+G` | Git integrado (Módulo 6!) |
| 🐞 | **Run and Debug** | `Ctrl+Shift+D` | Executar e depurar programas |
| 🧩 | **Extensions** | `Ctrl+Shift+X` | Instalar extensões (Módulo 4!) |

> 💡 Clicar no ícone ativo **esconde/mostra** a barra lateral. Também dá para alternar com `Ctrl+B` — útil para ganhar espaço na tela.

---

## 2.3 Explorer — o explorador de arquivos

O Explorer mostra a **árvore de arquivos** da pasta aberta. Por aqui você pode:

- **Criar arquivo:** botão 📄+ no topo, ou clique direito → *New File*
- **Criar pasta:** botão 📁+ no topo, ou clique direito → *New Folder*
- **Renomear:** selecione e pressione `F2`
- **Excluir:** selecione e pressione `Delete`
- **Arrastar e soltar** para mover arquivos entre pastas

> 💡 **Truque:** ao criar um arquivo, digite o caminho completo com barras: `src/utils/ajuda.js` — o VS Code cria as pastas `src` e `utils` automaticamente!

### Indicadores visuais nos arquivos

Repare nas **cores e letras** ao lado dos nomes dos arquivos quando o projeto usa Git:

- **Verde + U** (Untracked) — arquivo novo, ainda não rastreado
- **Amarelo/laranja + M** (Modified) — arquivo modificado desde o último commit
- **Ponto ●** na aba — arquivo com alterações **não salvas**

---

## 2.4 O Editor

É a área central, onde o código acontece.

### Abas e grupos de editores

- Cada arquivo aberto vira uma **aba**
- `Ctrl+Tab` alterna entre abas abertas
- `Ctrl+W` fecha a aba atual
- **Dividir a tela:** arraste uma aba para a lateral, ou use `Ctrl+\` — ótimo para comparar dois arquivos lado a lado

### Modo preview (itálico na aba)

Ao clicar **uma vez** em um arquivo no Explorer, ele abre em *modo preview* (nome em **itálico** na aba). Se você clicar em outro arquivo, ele **substitui** a aba. Para fixar:

- Dê **duplo clique** no arquivo, ou
- Dê duplo clique na própria aba, ou
- Comece a editar o arquivo

### Minimapa

A coluna estreita à direita é o **minimapa** — uma visão em miniatura do arquivo inteiro. Útil em arquivos longos. Pode ser desativado em `View → Appearance → Minimap`.

### Breadcrumbs (migalhas de pão)

Logo acima do código há uma trilha como `src > utils > ajuda.js > minhaFuncao`. Clicar em cada parte permite **navegar** pela estrutura do arquivo e do projeto.

---

## 2.5 A Paleta de Comandos — o recurso mais importante do VS Code

Se você só puder decorar **um atalho**, que seja este:

<div align="center">

## `Ctrl+Shift+P`

</div>

A **Command Palette** (paleta de comandos) dá acesso a **tudo** que o VS Code faz, sem precisar decorar menus. Basta digitar o que você quer:

- `settings` → abre as configurações
- `theme` → troca o tema de cores
- `terminal` → abre o terminal
- `format` → formata o documento

> 💡 A paleta usa **busca aproximada** (fuzzy search): digitar `fmt doc` já encontra "Format Document".

### A prima da paleta: Quick Open

`Ctrl+P` (sem Shift) abre o **Quick Open** — busca rápida de **arquivos** pelo nome:

- Digite `ajuda` → encontra `src/utils/ajuda.js`
- Digite `:25` → vai para a linha 25 do arquivo atual
- Digite `@` → lista os símbolos (funções, classes) do arquivo atual
- Digite `?` → mostra tudo que o Quick Open pode fazer

| Atalho | O que abre | Busca por... |
|--------|-----------|--------------|
| `Ctrl+P` | Quick Open | **arquivos** |
| `Ctrl+Shift+P` | Command Palette | **comandos** |

---

## 2.6 Painel inferior

Fica abaixo do editor. Abra/feche com `Ctrl+J`. Contém 4 guias principais:

| Guia | Para quê |
|------|----------|
| **Problems** | Lista erros e avisos do código (clique para ir até a linha) |
| **Output** | Mensagens das ferramentas e extensões |
| **Debug Console** | Saída durante a depuração |
| **Terminal** | Terminal integrado (Módulo 5!) |

---

## 2.7 Barra de Status

A faixa azul (ou colorida) no rodapé traz informações úteis. Da esquerda para a direita:

- 🔀 **Branch do Git** atual (ex.: `main`) — clicar permite trocar de branch!
- ⚠️ Contagem de **erros e avisos**
- **Linha e coluna** do cursor (`Ln 12, Col 8`)
- **Codificação** do arquivo (UTF-8)
- **Linguagem** detectada (JavaScript, Java...) — clicar permite mudar

> ⚠️ Se o código não estiver colorido corretamente, verifique aqui se a linguagem foi detectada certa!

---

## 2.8 Modo Zen e tela cheia
z
Para apresentações ou foco total:

- `F11` — tela cheia
- `Ctrl+K Z` — **Modo Zen** (esconde tudo, só o código; `Esc Esc` para sair)

---

## ✅ Checklist do módulo

- [ ] Sei alternar entre Explorer, Busca, Git e Extensões
- [ ] Sei abrir a paleta de comandos (`Ctrl+Shift+P`)
- [ ] Sei buscar arquivos pelo nome (`Ctrl+P`)
- [ ] Sei abrir o terminal/painel (`Ctrl+J`)
- [ ] Identifico a branch do Git na barra de status

## ✏️ Exercícios

Faça os [exercícios do Módulo 2](exercicios/README.md#módulo-2).

---

[← Módulo anterior](01-introducao-instalacao.md) | [Voltar ao índice](README.md) | [Próximo módulo →](03-edicao-produtiva.md)
