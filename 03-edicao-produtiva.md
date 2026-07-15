# Módulo 3 — Edição Produtiva

[← Módulo anterior](02-interface.md) | [Voltar ao índice](README.md) | [Próximo módulo →](04-extensoes.md)

---

> 🎯 **Meta deste módulo:** escrever e modificar código mais rápido, tirando as mãos do mouse.

## 3.1 Atalhos essenciais de edição

Estes são os atalhos que **mais economizam tempo** no dia a dia. Pratique um por vez!

### Manipulando linhas

| Atalho | Ação |
|--------|------|
| `Ctrl+C` (sem seleção) | Copia a **linha inteira** |
| `Ctrl+X` (sem seleção) | Recorta a **linha inteira** (funciona como "excluir linha") |
| `Shift+Alt+↓` / `Shift+Alt+↑` | **Duplica** a linha para baixo/cima |
| `Alt+↓` / `Alt+↑` | **Move** a linha para baixo/cima |
| `Ctrl+Shift+K` | Exclui a linha |
| `Ctrl+Enter` | Insere linha nova **abaixo** (sem quebrar a atual) |
| `Ctrl+Shift+Enter` | Insere linha nova **acima** |

> 💡 `Alt+↑/↓` é viciante: reordene linhas de código sem copiar e colar nada.

### Comentários

| Atalho | Ação |
|--------|------|
| `Ctrl+;` ou `Ctrl+/` * | Comenta/descomenta a linha (`//` em JS e Java) |
| `Shift+Alt+A` | Comentário de bloco (`/* ... */`) |

> \* Em teclados ABNT (padrão brasileiro), o atalho de comentário costuma ser `Ctrl+;` — teste no seu teclado! Nos teclados internacionais é `Ctrl+/`.

### Navegação no código

| Atalho | Ação |
|--------|------|
| `Ctrl+G` | Ir para a linha N |
| `Ctrl+Home` / `Ctrl+End` | Início / fim do arquivo |
| `F12` | Ir para a **definição** de uma função/variável |
| `Alt+←` | Voltar para onde estava (após um F12, por exemplo) |
| `Ctrl+Shift+O` | Listar símbolos do arquivo (funções, classes) |

---

## 3.2 Seleção inteligente

| Atalho | Ação |
|--------|------|
| Duplo clique | Seleciona a palavra |
| Triplo clique | Seleciona a linha |
| `Ctrl+L` | Seleciona a linha inteira (e expande a cada aperto) |
| `Shift+Alt+→` | **Expande** a seleção por escopo (palavra → expressão → bloco → função) |
| `Shift+Alt+←` | Encolhe a seleção |
| `Ctrl+A` | Seleciona tudo |

> 💡 `Shift+Alt+→` é ótimo para selecionar todo o conteúdo de um par de chaves `{ }` sem contar linhas.

---

## 3.3 Multicursor — editando vários lugares ao mesmo tempo

O recurso que mais impressiona quem vem de editores simples. **Vários cursores digitam simultaneamente.**

### Formas de criar múltiplos cursores

| Atalho | Ação |
|--------|------|
| `Alt+Clique` | Adiciona um cursor onde você clicar |
| `Ctrl+Alt+↓` / `Ctrl+Alt+↑` | Adiciona cursor na linha abaixo/acima |
| `Ctrl+D` | Seleciona a **próxima ocorrência** da palavra sob o cursor |
| `Ctrl+Shift+L` | Seleciona **todas** as ocorrências da palavra |
| `Esc` | Volta a um cursor só |

### Exemplo prático com `Ctrl+D`

Imagine que você quer renomear a variável `valor` para `preco` nestas linhas:

```javascript
let valor = 10;
let total = valor * 2;
console.log(valor, total);
```

1. Dê duplo clique em `valor` (primeira ocorrência)
2. Pressione `Ctrl+D` duas vezes — as outras duas ocorrências são selecionadas
3. Digite `preco` — as três mudam ao mesmo tempo!

> ⚠️ **Cuidado:** `Ctrl+D` seleciona por **texto**, não por significado. Para renomear variáveis com segurança (respeitando escopo), use `F2` (**Rename Symbol**) — o VS Code renomeia todas as referências *reais* da variável, inclusive em outros arquivos.

---

## 3.4 Busca e substituição

### No arquivo atual

| Atalho | Ação |
|--------|------|
| `Ctrl+F` | Buscar |
| `Ctrl+H` | Buscar e **substituir** |
| `Enter` / `Shift+Enter` | Próxima / anterior ocorrência |

Na caixinha de busca, repare nos três botões:

- **Aa** — diferenciar maiúsculas/minúsculas (case sensitive)
- **ab** — palavra inteira apenas
- **.\*** — expressões regulares (regex)

### No projeto inteiro

`Ctrl+Shift+F` busca em **todos os arquivos** da pasta. Com `Ctrl+Shift+H`, substitui em todos.

> ⚠️ Substituição em massa no projeto inteiro é poderosa e perigosa. Revise a prévia antes de aplicar — e é para isso que existe o Git, certo? 😉

---

## 3.5 IntelliSense — o autocompletar inteligente

Ao digitar, o VS Code sugere variáveis, funções e métodos. Isso se chama **IntelliSense**.

- `Ctrl+Espaço` — força a exibição das sugestões
- `Tab` ou `Enter` — aceita a sugestão selecionada
- Passe o mouse sobre uma função para ver a **documentação** dela
- `Ctrl+Shift+Espaço` — mostra os **parâmetros** da função enquanto você a chama

Em JavaScript, digite `document.` ou `console.` e veja a lista de métodos disponíveis. Em Java (com a extensão do Módulo 4), o IntelliSense conhece toda a biblioteca padrão.

---

## 3.6 Formatação automática

Código bem indentado é requisito, não luxo. O VS Code formata para você:

| Atalho | Ação |
|--------|------|
| `Shift+Alt+F` | **Formatar o documento** inteiro |
| `Ctrl+K Ctrl+F` | Formatar só a seleção |

### Formatar ao salvar (recomendado!)

1. `Ctrl+,` para abrir Settings
2. Busque `format on save`
3. Marque ✅ **Editor: Format On Save**

A partir daí, todo `Ctrl+S` deixa o código formatado. No Módulo 4 veremos o **Prettier**, que melhora ainda mais a formatação de JavaScript.

---

## 3.7 Desfazer, refazer e a linha do tempo

- `Ctrl+Z` — desfazer
- `Ctrl+Y` (ou `Ctrl+Shift+Z`) — refazer
- **Timeline:** no Explorer, o painel *Timeline* (embaixo) guarda um histórico local de versões do arquivo — pode salvar sua vida antes mesmo do Git!

---

## ✅ Checklist do módulo

- [ ] Sei mover e duplicar linhas com `Alt+↑/↓` e `Shift+Alt+↑/↓`
- [ ] Sei comentar código com atalho
- [ ] Usei multicursor com `Ctrl+D`
- [ ] Sei a diferença entre `Ctrl+D` e `F2` (Rename Symbol)
- [ ] Ativei o Format On Save

## ✏️ Exercícios

Faça os [exercícios do Módulo 3](exercicios/README.md#módulo-3) — este módulo é o que mais exige prática!

---

[← Módulo anterior](02-interface.md) | [Voltar ao índice](README.md) | [Próximo módulo →](04-extensoes.md)
