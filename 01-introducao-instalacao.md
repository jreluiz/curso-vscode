# Módulo 1 — Introdução e Instalação

[← Voltar ao índice](README.md) | [Próximo módulo →](02-interface.md)

---

## 1.1 O que é o VS Code?

O **Visual Studio Code** (ou apenas **VS Code**) é um **editor de código-fonte** gratuito, de código aberto e multiplataforma, desenvolvido pela Microsoft. É hoje o editor mais usado no mundo por desenvolvedores profissionais.

### Editor de código ≠ IDE ≠ editor de texto

É comum confundir esses três conceitos:v

| Ferramenta | Exemplo | Característica |
|------------|---------|----------------|
| **Editor de texto** | Bloco de Notas | Só edita texto puro, sem recursos para programação |
| **Editor de código** | VS Code, Sublime | Leve, com destaque de sintaxe, autocompletar e extensões |
| **IDE** | IntelliJ, Eclipse, NetBeans | Ambiente completo e pesado, com compilador, debugger e ferramentas integradas de fábrica |

O VS Code fica em um meio-termo interessante: **nasce leve como um editor**, mas com extensões pode se aproximar do poder de uma IDE. Por isso ele serve tanto para JavaScript quanto para Java, Python, C e praticamente qualquer linguagem.

### Por que usar o VS Code?

- 🆓 **Gratuito** — sem licenças ou versões "trial"
- 🪶 **Leve** — roda bem até em máquinas modestas do laboratório
- 🌍 **Universal** — o mesmo editor para JavaScript, Java, HTML, CSS, Markdown...
- 🧩 **Extensível** — instalamos só o que precisamos
- 🔀 **Git integrado** — controle de versão direto no editor
- 💼 **Mercado** — é a ferramenta que você provavelmente usará profissionalmente

> ⚠️ **Atenção:** não confunda **Visual Studio Code** com **Visual Studio**. O Visual Studio (sem "Code") é uma IDE completa e pesada, voltada principalmente para C# e .NET. São produtos diferentes!

---

## 1.2 Instalação

### Windows

1. Acesse o site oficial: **https://code.visualstudio.com**
2. Clique em **Download for Windows**
3. Execute o instalador baixado (`VSCodeUserSetup-x64-*.exe`)
4. Durante a instalação, **marque estas opções** (importantes!):
   - ✅ *Adicionar ação "Abrir com Code" ao menu de contexto de arquivo*
   - ✅ *Adicionar ação "Abrir com Code" ao menu de contexto de diretório*
   - ✅ *Adicionar ao PATH*
5. Conclua e abra o VS Code

> 💡 A opção "Adicionar ao PATH" permite abrir o VS Code pelo terminal digitando `code .` — vamos usar muito isso!

### Linux (Ubuntu/Debian)

Pela loja de aplicativos (mais simples) ou pelo terminal:

```bash
# Baixar e instalar o pacote .deb
sudo apt update
sudo apt install wget gpg
wget -O vscode.deb "https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64"
sudo apt install ./vscode.deb
```

### macOS

1. Baixe o `.zip` em **https://code.visualstudio.com**
2. Extraia e arraste o **Visual Studio Code.app** para a pasta **Aplicativos**
3. Para habilitar o comando `code` no terminal: abra o VS Code, pressione `Cmd+Shift+P`, digite `shell command` e escolha **Install 'code' command in PATH**

### 💻 E no laboratório?

Nos computadores do laboratório o VS Code **já está instalado**. Como o ambiente é compartilhado, lembre-se:

- Salve seus arquivos **na sua pasta pessoal ou pendrive** (e faça push para o GitHub!)
- **Não salve senhas** no navegador ou no editor
- Ao final da aula, **deslogue** de qualquer conta (GitHub, etc.)

---

## 1.3 Primeiro contato

### Mudando o idioma para português (opcional)

O VS Code vem em inglês por padrão. Se preferir português:

1. Pressione `Ctrl+Shift+P` (abre a **paleta de comandos** — nossa melhor amiga!)
2. Digite `display language`
3. Escolha **Configure Display Language**
4. Selecione **Português (Brasil)** — o editor baixará o pacote de idioma e reiniciará

> 📝 **Nota:** este material usa os nomes de menus **em inglês**, pois é o padrão da documentação e do mercado. Entre parênteses, indicamos a tradução quando relevante.

### Abrindo uma pasta de projeto

O VS Code trabalha com o conceito de **pasta de trabalho** (workspace). Em vez de abrir arquivos soltos, você abre a **pasta do projeto inteiro**:

**Opção 1 — pelo menu:**
`File → Open Folder...` (Arquivo → Abrir Pasta)

**Opção 2 — pelo terminal (a preferida dos devs):**

```bash
cd meu-projeto
code .
```

O `.` significa "a pasta atual". Esse comando abre o VS Code já com o projeto carregado.

**Opção 3 — pelo menu de contexto (Windows):**
Clique com o botão direito na pasta → **Abrir com Code**

### Criando seu primeiro arquivo

1. Com uma pasta aberta, pressione `Ctrl+N` (novo arquivo)
2. Digite:
   ```javascript
   console.log("Olá, VS Code!");
   ```
3. Salve com `Ctrl+S` e nomeie como `ola.js`
4. Repare que, ao salvar com a extensão `.js`, o editor **reconhece a linguagem** e colore o código (syntax highlighting)

---

## ✅ Checklist do módulo

- [ ] Instalei o VS Code (ou localizei no laboratório)
- [ ] Sei a diferença entre editor de código e IDE
- [ ] Abri uma pasta de projeto com `code .`
- [ ] Criei e salvei um arquivo `.js`

## ✏️ Exercícios

Faça os [exercícios do Módulo 1](exercicios/README.md#módulo-1).

---

[← Voltar ao índice](README.md) | [Próximo módulo →](02-interface.md)
