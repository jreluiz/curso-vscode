---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 3'
---

<!-- _class: capa -->

<div class="emoji">⚡</div>

# Edição Produtiva

## Módulo 3 · Curso de VS Code

<div class="meta">Escrever mais rápido, tirando as mãos do mouse</div>

---

<!-- _class: lead -->

## 🎯 A meta deste módulo

Cada vez que a sua mão sai do teclado
e vai até o mouse, você perde tempo.

Este módulo é sobre **não sair do teclado**.

Pratique **um atalho por vez** — decorar dez de uma vez não funciona.

---

<!-- _class: tabela-densa -->

## Manipulando linhas

| Atalho | Ação |
|---|---|
| `Ctrl+C` sem seleção | copia a **linha inteira** |
| `Ctrl+X` sem seleção | recorta a linha — funciona como "excluir linha" |
| `Alt+↓` / `Alt+↑` | **move** a linha para baixo / cima |
| `Shift+Alt+↓` / `↑` | **duplica** a linha |
| `Ctrl+Shift+K` | exclui a linha |
| `Ctrl+Enter` | nova linha **abaixo**, sem quebrar a atual |

> 💡 `Alt+↑/↓` é viciante: reordene código sem copiar e colar nada.

---

<!-- _class: tabela-densa -->

## Comentários e navegação

| Atalho | Ação |
|---|---|
| `Ctrl+;` ou `Ctrl+/` | comenta / descomenta a linha |
| `Shift+Alt+A` | comentário de bloco `/* ... */` |
| `Ctrl+G` | ir para a linha N |
| `F12` | ir para a **definição** da função |
| `Alt+←` | **voltar** para onde você estava |

> ⚠️ Em teclado **ABNT**, o atalho de comentário costuma ser `Ctrl+;`. Nos internacionais, `Ctrl+/`. Teste no seu.

---

<!-- _class: tabela-densa -->

## Seleção inteligente

| Atalho | Ação |
|---|---|
| Duplo clique | seleciona a palavra |
| `Ctrl+L` | seleciona a linha — e expande a cada aperto |
| `Shift+Alt+→` | **expande por escopo**: palavra → expressão → bloco → função |
| `Shift+Alt+←` | encolhe a seleção |

> 💡 `Shift+Alt+→` seleciona todo o conteúdo de um par de chaves `{ }` sem você contar uma linha sequer.

---

<!-- _class: lead -->

## 🤯 Multicursor

O recurso que mais impressiona
quem vem de um editor simples.

**Vários cursores digitando ao mesmo tempo.**

---

## Como criar vários cursores

| Atalho | Ação |
|---|---|
| `Alt+Clique` | adiciona um cursor onde você clicar |
| `Ctrl+Alt+↓` / `↑` | adiciona cursor na linha abaixo / acima |
| `Ctrl+D` | seleciona a **próxima ocorrência** da palavra |
| `Ctrl+Shift+L` | seleciona **todas** as ocorrências |
| `Esc` | volta a um cursor só |

---

## `Ctrl+D` na prática

Renomear `valor` para `preco` nestas três linhas:

```javascript
let valor = 10;
let total = valor * 2;
console.log(valor, total);
```

1. Duplo clique em `valor`;
2. `Ctrl+D` duas vezes — as outras ocorrências entram na seleção;
3. Digite `preco` — as três mudam juntas.

---

<!-- _class: lead -->

## ⚠️ `Ctrl+D` × `F2`

`Ctrl+D` seleciona por **texto**.
Não sabe o que é variável, o que é comentário.

`F2` é **Rename Symbol**: renomeia as referências **reais** da variável, respeitando escopo — inclusive em outros arquivos.

Para renomear de verdade, use **`F2`**.

---

## Busca e substituição

| Atalho | Onde |
|---|---|
| `Ctrl+F` / `Ctrl+H` | buscar / substituir **no arquivo** |
| `Ctrl+Shift+F` / `Ctrl+Shift+H` | buscar / substituir **no projeto inteiro** |

Na caixa de busca, três botões: **Aa** maiúsculas · **ab** palavra inteira · **.\*** regex.

> ⚠️ Substituir no projeto inteiro é poderoso e perigoso. Revise a prévia antes de aplicar — e é para isso que existe o Git.

---

## IntelliSense — o autocompletar que entende

| Atalho | Ação |
|---|---|
| `Ctrl+Espaço` | força a exibição das sugestões |
| `Tab` ou `Enter` | aceita a sugestão |
| `Ctrl+Shift+Espaço` | mostra os **parâmetros** da função |

Passe o mouse sobre qualquer função para ler a documentação dela ali mesmo.

> 💡 Digite `console.` num arquivo `.js` e veja a lista aparecer.

---

## Formatação automática

| Atalho | Ação |
|---|---|
| `Shift+Alt+F` | formata o **documento inteiro** |
| `Ctrl+K Ctrl+F` | formata só a seleção |

**Melhor ainda — formatar ao salvar:**

`Ctrl+,` → busque `format on save` → marque ✅ **Editor: Format On Save**

A partir daí, todo `Ctrl+S` deixa o código indentado.

---

## Desfazer — e a rede de segurança

- `Ctrl+Z` desfaz · `Ctrl+Y` refaz;
- **Timeline:** no Explorer, o painel *Timeline* guarda um histórico local do arquivo.

> 💡 A Timeline já salvou muita gente **antes** do primeiro commit. Mas não substitui o Git: ela é local, individual e temporária.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Sei mover e duplicar linhas com `Alt+↑↓` e `Shift+Alt+↑↓`;
- ☐ Sei comentar código por atalho;
- ☐ Usei multicursor com `Ctrl+D`;
- ☐ Sei a diferença entre `Ctrl+D` e `F2`;
- ☐ Ativei o **Format On Save**.

---

<!-- _class: lead -->

## ➡️ Próximo passo

**Módulo 4 — Extensões**

O superpoder do editor —
e como não instalar coisa perigosa.
