# Módulo 4 — Extensões

[← Módulo anterior](03-edicao-produtiva.md) | [Voltar ao índice](README.md) | [Próximo módulo →](05-terminal-integrado.md)

---

## 4.1 O que são extensões?

O VS Code "puro" já é bom, mas seu superpoder são as **extensões**: pacotes que adicionam suporte a linguagens, temas, atalhos e ferramentas. É como uma loja de aplicativos dentro do editor.

### Como instalar

1. Clique no ícone 🧩 na barra de atividades (ou `Ctrl+Shift+X`)
2. Digite o nome da extensão na busca
3. Clique em **Install**

Pronto — sem baixar nada manualmente, sem reiniciar (na maioria dos casos).

### Como avaliar se uma extensão é confiável

Antes de instalar, observe na página da extensão:

- 👤 **Publicador verificado** (selinho azul) — ex.: Microsoft, Red Hat
- ⬇️ **Número de downloads** — milhões de instalações indicam maturidade
- ⭐ **Avaliações** — leia os comentários recentes
- 📅 **Última atualização** — extensões abandonadas podem ter problemas

> ⚠️ **Segurança:** extensões executam código no seu computador. Extensões maliciosas existem e já foram encontradas no marketplace, inclusive imitando nomes de extensões famosas (typosquatting). Instale apenas o necessário, prefira publicadores verificados e desconfie de extensões novas com nomes "quase iguais" às populares. Na dúvida, verifique bem cada extensão antes de instalar algo fora da lista abaixo.

---

## 4.2 Extensões essenciais por linguagem

### 📦 Para JavaScript / Node.js

| Extensão                           | Publicador            | Para quê                                                       |
| ---------------------------------- | --------------------- | -------------------------------------------------------------- |
| **Prettier – Code formatter**      | Prettier              | Formatação automática e consistente do código                  |
| **ESLint**                         | Microsoft             | Aponta erros e más práticas no JavaScript enquanto você digita |
| **JavaScript (ES6) code snippets** | charalampos karypidis | Atalhos para trechos comuns de código                          |

### ☕ Para Java

| Extensão                    | Publicador | Para quê                                                              |
| --------------------------- | ---------- | --------------------------------------------------------------------- |
| **Extension Pack for Java** | Microsoft  | Pacote completo: suporte à linguagem, executar/debugar, testes, Maven |

> 💡 O _Extension Pack for Java_ instala **6 extensões de uma vez** (Language Support, Debugger, Test Runner, Maven, Project Manager e IntelliCode). É tudo que você precisa para programar em Java.
>
> ⚠️ **Pré-requisito:** para programar em Java, você precisa do **JDK** instalado (versão 17 ou superior). A extensão avisa e oferece ajuda para instalar se não encontrar.

### 🌐 Para HTML/CSS

| Extensão        | Publicador  | Para quê                                                          |
| --------------- | ----------- | ----------------------------------------------------------------- |
| **Live Server** | Ritwick Dey | Abre sua página no navegador com **recarga automática** ao salvar |

### 🔀 Para Git (complementa o Módulo 6)

| Extensão      | Publicador | Para quê                                                        |
| ------------- | ---------- | --------------------------------------------------------------- |
| **GitLens**   | GitKraken  | Mostra quem alterou cada linha (blame), histórico visual e mais |
| **Git Graph** | mhutchie   | Gráfico visual das branches e commits                           |

### 📝 Para Markdown (útil para os READMEs dos projetos!)

O VS Code já tem **preview de Markdown nativo**: abra um `.md` e pressione `Ctrl+Shift+V` (ou `Ctrl+K V` para ver lado a lado). Para recursos extras:

| Extensão                | Publicador | Para quê                                           |
| ----------------------- | ---------- | -------------------------------------------------- |
| **Markdown All in One** | Yu Zhang   | Atalhos, sumário automático, formatação de tabelas |

### 🎨 Aparência (opcional, mas todo mundo gosta)

| Extensão                                | Para quê                                          |
| --------------------------------------- | ------------------------------------------------- |
| **Material Icon Theme**                 | Ícones bonitos para arquivos e pastas no Explorer |
| **One Dark Pro** / **Dracula Official** | Temas de cores populares                          |

---

## 4.3 Configurando o Prettier como formatador padrão

Depois de instalar o Prettier:

1. `Ctrl+Shift+P` → digite `settings json` → **Preferences: Open User Settings (JSON)**
2. Adicione:

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```

Agora todo arquivo JS/HTML/CSS/JSON é formatado ao salvar, no padrão usado pela indústria.

---

## 4.4 Gerenciando extensões

- **Desativar** em vez de desinstalar: clique na engrenagem da extensão → _Disable_. Útil para testar se uma extensão está causando lentidão.
- **Desativar só em um workspace:** _Disable (Workspace)_ — a extensão continua ativa nos outros projetos.
- **Extensões recomendadas por projeto:** um arquivo `.vscode/extensions.json` na raiz do projeto pode listar recomendações. Ao abrir a pasta, o VS Code sugere instalar. Exemplo:

```json
{
  "recommendations": [
    "esbenp.prettier-vscode",
    "dbaeumer.vscode-eslint",
    "vscjava.vscode-java-pack"
  ]
}
```

## ✅ Checklist do módulo

- [ ] Instalei o Prettier e o ESLint
- [ ] Instalei o Extension Pack for Java
- [ ] Instalei o Live Server
- [ ] Sei verificar se um publicador é confiável
- [ ] Configurei o Prettier como formatador padrão

## ✏️ Exercícios

Faça os [exercícios do Módulo 4](exercicios/README.md#módulo-4).

---

[← Módulo anterior](03-edicao-produtiva.md) | [Voltar ao índice](README.md) | [Próximo módulo →](05-terminal-integrado.md)
