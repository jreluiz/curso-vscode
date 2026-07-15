# Módulo 5 — Terminal Integrado

[← Módulo anterior](04-extensoes.md) | [Voltar ao índice](README.md) | [Próximo módulo →](06-git-github-no-vscode.md)

---

## 5.1 Por que um terminal dentro do editor?

Programar envolve alternar o tempo todo entre **escrever código** e **executar comandos** (rodar o programa, instalar pacotes, usar o Git). Com o terminal integrado, tudo acontece na mesma janela — e o terminal **já abre na pasta do projeto**.

## 5.2 Abrindo e controlando o terminal

| Atalho | Ação |
|--------|------|
| `Ctrl+'` (ou `Ctrl+J`) | Abre/fecha o terminal * |
| Botão **+** | Cria um novo terminal |
| Botão 🗑️ | Encerra o terminal atual |
| Ícone de divisão | Divide em dois terminais lado a lado |
| Lista suspensa | Alterna entre terminais abertos |

> \* O atalho oficial é `` Ctrl+` `` (crase), mas em teclados ABNT ele varia. `Ctrl+J` (abre o painel) funciona em qualquer teclado. Você também pode abrir por `Terminal → New Terminal` no menu.

### Qual shell está rodando?

O terminal integrado é um terminal **de verdade** — ele roda o shell do seu sistema:

- **Windows:** PowerShell (padrão) — ou Git Bash, se instalado
- **Linux/Mac:** bash ou zsh

> 💡 **Recomendação para Windows:** se você instalou o Git, pode usar o **Git Bash** como terminal padrão e ter os mesmos comandos do Linux. `Ctrl+Shift+P` → `Terminal: Select Default Profile` → escolha **Git Bash**.

## 5.3 Rodando JavaScript com Node.js

Com o Node.js instalado, execute qualquer arquivo `.js`:

```bash
# Verificar se o Node está instalado
node --version

# Executar um arquivo
node ola.js
```

Fluxo típico de trabalho com JavaScript:

1. Edite o arquivo no editor
2. `Ctrl+S` para salvar
3. `Ctrl+J` para focar o terminal
4. `node arquivo.js` (dica: `↑` repete o último comando!)
5. Veja a saída, volte ao código, repita

> 💡 **Preguiça produtiva:** digite `node ` e apenas **arraste o arquivo** do Explorer para o terminal — o caminho é preenchido automaticamente.

## 5.4 Rodando Java

Com o JDK e o Extension Pack for Java instalados, há duas formas:

### Pelo botão Run (mais fácil)

Ao abrir um arquivo com método `main`, aparece um botão **Run** ▶️ acima dele. Clique e pronto — o VS Code compila e executa no terminal.

### Pelo terminal (entendendo o processo)

```bash
# Compilar (gera o .class)
javac Pessoa.java

# Executar (repare: sem a extensão!)
java Pessoa
```

> 📚 **Por dentro:** esses dois passos são a compilação para *bytecode* e a execução na JVM. O terminal deixa esse processo visível, coisa que o botão Run esconde.

## 5.5 Comandos de terminal que você vai usar todo dia

Se você já usou o terminal, vários vão parecer familiares:

| Comando | Ação |
|---------|------|
| `pwd` | Mostra a pasta atual |
| `ls` (ou `dir` no PowerShell) | Lista os arquivos |
| `cd nome-da-pasta` | Entra na pasta |
| `cd ..` | Volta uma pasta |
| `mkdir nome` | Cria uma pasta |
| `clear` (ou `Ctrl+L`) | Limpa a tela |
| `↑` / `↓` | Navega no histórico de comandos |
| `Tab` | Autocompleta nomes de arquivos |

> ⚠️ **Copiar e colar no terminal:** `Ctrl+C` no terminal **interrompe o programa em execução**! Para copiar/colar, use `Ctrl+Shift+C` e `Ctrl+Shift+V` (ou clique direito).

## 5.6 Encerrando programas travados

Se um programa ficar rodando para sempre (um loop infinito acontece com os melhores de nós 😄):

- `Ctrl+C` no terminal — interrompe o processo
- Se não resolver: clique no 🗑️ para matar o terminal e abra outro

---

## ✅ Checklist do módulo

- [ ] Sei abrir e fechar o terminal integrado
- [ ] Executei um arquivo `.js` com `node`
- [ ] Executei uma classe Java (pelo botão Run e pelo terminal)
- [ ] Sei interromper um programa com `Ctrl+C`
- [ ] Sei usar `↑` e `Tab` para digitar menos

## ✏️ Exercícios

Faça os [exercícios do Módulo 5](exercicios/README.md#módulo-5).

---

[← Módulo anterior](04-extensoes.md) | [Voltar ao índice](README.md) | [Próximo módulo →](06-git-github-no-vscode.md)
