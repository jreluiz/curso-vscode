---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 1'
---

<!-- _class: capa -->

<div class="emoji">🔵</div>

# Introdução e Instalação

## Módulo 1 · Curso de VS Code

<div class="meta">O editor mais usado do mundo — do zero ao primeiro arquivo</div>

---

## Roteiro

1. O que é o VS Code — e o que **não** é
2. Por que ele virou padrão de mercado
3. Instalar no Windows, Linux e macOS
4. Abrir um projeto e criar o primeiro arquivo

---

## Editor de texto ≠ editor de código ≠ IDE

| Ferramenta | Exemplo | Característica |
|---|---|---|
| **Editor de texto** | Bloco de Notas | só texto puro, nada para programar |
| **Editor de código** | VS Code, Sublime | leve, com sintaxe colorida, autocompletar e extensões |
| **IDE** | IntelliJ, Eclipse | ambiente completo e pesado, tudo de fábrica |

O VS Code fica no meio-termo: **nasce leve como editor**, mas com extensões chega perto de uma IDE.

---

<!-- _class: lista-limpa -->

## Por que usar o VS Code

- 🆓 **Gratuito** — sem licença, sem versão *trial*;
- 🪶 **Leve** — roda bem em máquina modesta;
- 🌍 **Universal** — o mesmo editor para JavaScript, Java, HTML, CSS, Markdown;
- 🧩 **Extensível** — você instala só o que precisa;
- 🔀 **Git integrado** — controle de versão dentro do editor;
- 💼 **Mercado** — é a ferramenta que você provavelmente usará profissionalmente.

---

<!-- _class: lead -->

## ⚠️ Visual Studio Code ≠ Visual Studio

**Visual Studio** (sem "Code") é uma IDE completa e pesada, voltada a C# e .NET.

São **produtos diferentes**, de nomes parecidos.

Ao baixar, confira que está em `code.visualstudio.com`.

---

## Instalando — Windows

1. Baixe em `code.visualstudio.com` → **Download for Windows**;
2. Execute o instalador;
3. **Marque estas opções** — elas importam:
   - ✅ *Abrir com Code* no menu de contexto de **arquivo**
   - ✅ *Abrir com Code* no menu de contexto de **pasta**
   - ✅ **Adicionar ao PATH**

> 💡 O "Adicionar ao PATH" é o que permite abrir o editor digitando `code .` no terminal — usaremos muito isso.

---

## Instalando — Linux e macOS

**Linux** (Ubuntu/Debian) — pela loja de aplicativos, ou:

```bash
sudo apt install wget gpg
wget -O vscode.deb "https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64"
sudo apt install ./vscode.deb
```

**macOS** — baixe o `.zip`, arraste para **Aplicativos**. Para habilitar o comando `code`:

`Cmd+Shift+P` → `shell command` → **Install 'code' command in PATH**

---

<!-- _class: lista-limpa -->

## Em computador compartilhado

O ambiente é de todos — três cuidados:

- 💾 Salve na **sua pasta pessoal ou pendrive** — e faça `push` para o GitHub;
- 🔑 **Não salve senhas** no navegador nem no editor;
- 🚪 Ao terminar, **deslogue** de todas as contas.

---

## A paleta de comandos, desde já

Para mudar o idioma para português — e para praticamente tudo o mais:

**`Ctrl+Shift+P`** → digite `display language` → **Configure Display Language** → Português (Brasil)

> 📝 Este material usa os nomes de menu **em inglês**, que é o padrão da documentação e do mercado.

---

## Abrindo uma pasta de projeto

O VS Code trabalha com **pasta**, não com arquivo solto. Três caminhos:

```bash
cd meu-projeto
code .            # o "." significa: a pasta atual
```

- **Menu:** `File → Open Folder...`
- **Windows:** botão direito na pasta → *Abrir com Code*

---

## O primeiro arquivo

1. Com a pasta aberta, `Ctrl+N` — novo arquivo;
2. Digite:

```javascript
console.log("Olá, VS Code!");
```

3. `Ctrl+S` e salve como `ola.js`.

Ao salvar com a extensão `.js`, o editor **reconhece a linguagem** e colore o código.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Instalei o VS Code — ou localizei no computador que vou usar;
- ☐ Sei a diferença entre editor de código e IDE;
- ☐ Abri uma pasta de projeto com `code .`;
- ☐ Criei e salvei um arquivo `.js`.

---

<!-- _class: lead -->

## ➡️ Próximo passo

**Módulo 2 — Conhecendo a Interface**

As seis regiões da janela, a barra de atividades
e o atalho mais importante do editor.
