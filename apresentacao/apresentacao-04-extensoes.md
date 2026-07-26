---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 4'
---

<!-- _class: capa -->

<div class="emoji">🧩</div>

# Extensões

## Módulo 4 · Curso de VS Code

<div class="meta">O superpoder do editor — e como não instalar coisa perigosa</div>

---

## Roteiro

1. O que são extensões e como instalar
2. **Como avaliar se uma extensão é confiável**
3. As essenciais por linguagem
4. Prettier como formatador padrão
5. Gerenciar e recomendar por projeto

---

## O que são extensões

O VS Code "puro" já é bom. O superpoder são as **extensões**: pacotes que adicionam suporte a linguagens, temas, atalhos e ferramentas.

É uma loja de aplicativos dentro do editor.

**Instalar:** ícone 🧩 (`Ctrl+Shift+X`) → busque o nome → **Install**.

Sem baixar nada à mão e, na maioria dos casos, sem reiniciar.

---

<!-- _class: lista-limpa -->

## Antes de instalar, olhe quatro coisas

- 👤 **Publicador verificado** — o selinho azul. Microsoft, Red Hat, Prettier;
- ⬇️ **Downloads** — milhões de instalações indicam maturidade;
- ⭐ **Avaliações** — leia os comentários **recentes**;
- 📅 **Última atualização** — extensão abandonada dá problema.

---

<!-- _class: lead -->

## ⚠️ Extensão executa código na sua máquina

Extensões maliciosas existem e **já foram encontradas** no marketplace.

O golpe mais comum é o *typosquatting*: um nome quase igual ao de uma extensão famosa.

Instale só o necessário, prefira publicador verificado, e desconfie de nome parecido com poucos downloads.

---

## 📦 JavaScript e Node.js

| Extensão | Publicador | Para quê |
|---|---|---|
| **Prettier – Code formatter** | Prettier | formatação automática e consistente |
| **ESLint** | Microsoft | aponta erros e más práticas enquanto você digita |
| **JavaScript (ES6) code snippets** | charalampos karypidis | atalhos para trechos comuns |

---

## ☕ Java — um pacote resolve tudo

**Extension Pack for Java** (Microsoft) instala **seis extensões de uma vez**: suporte à linguagem, debugger, testes, Maven, gerenciador de projetos e IntelliCode.

> ⚠️ **Pré-requisito:** é preciso ter o **JDK 17 ou superior** instalado. A extensão avisa e ajuda a instalar se não encontrar.

---

## 🌐 Web, 🔀 Git e 📝 Markdown

| Extensão | Para quê |
|---|---|
| **Live Server** | abre a página no navegador com **recarga automática** ao salvar |
| **GitLens** | mostra quem alterou cada linha — o `git blame`, humanizado |
| **Git Graph** | gráfico visual das branches e commits |
| **Markdown All in One** | sumário automático, formatação de tabelas |

> 💡 O preview de Markdown já é **nativo**: `Ctrl+Shift+V`, ou `Ctrl+K V` para ver lado a lado.

---

## Prettier como formatador padrão

`Ctrl+Shift+P` → `settings json` → **Open User Settings (JSON)** e adicione:

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```

Todo arquivo JS, HTML, CSS e JSON passa a ser formatado ao salvar, no padrão da indústria.

---

<!-- _class: lista-limpa -->

## Gerenciando extensões

- ⏸️ **Desativar em vez de desinstalar** — engrenagem → *Disable*. Útil para descobrir qual extensão deixou o editor lento;
- 📁 **Desativar só num projeto** — *Disable (Workspace)*: continua ativa nos outros;
- 🎭 **Perfis** — conjuntos diferentes de extensões por contexto: um perfil "Java", um "Web".

---

## Recomendar extensões por projeto

Um arquivo `.vscode/extensions.json` na raiz sugere extensões a quem abrir a pasta:

```json
{
  "recommendations": [
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "vscjava.vscode-java-pack"
  ]
}
```

> 💡 Em trabalho de equipe isso vale ouro: todo mundo abre o projeto já com as mesmas ferramentas.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Instalei o Prettier e o ESLint;
- ☐ Instalei o Extension Pack for Java;
- ☐ Instalei o Live Server;
- ☐ Sei verificar se um publicador é confiável;
- ☐ Configurei o Prettier como formatador padrão.

---

<!-- _class: lead -->

## ➡️ Próximo passo

**Módulo 5 — Terminal Integrado**

Rodar o código sem sair do editor.
