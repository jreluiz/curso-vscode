---
marp: true
theme: trilha
paginate: true
lang: pt-BR
footer: '🔵 Curso de VS Code · Módulo 6'
---

<!-- _class: capa -->

<div class="emoji">🔀</div>

# Git e GitHub no VS Code

## Módulo 6 · Curso de VS Code

<div class="meta">Os comandos que você já conhece, agora em botões</div>

---

<!-- _class: lead -->

## 📚 Antes de começar

Este módulo assume que você já sabe
o básico de Git: `add`, `commit`, `push`, `pull`.

Aqui o VS Code vai **facilitar** o que você já sabe fazer no terminal.

**Não substituir o entendimento dos comandos.**

---

<!-- _class: lead -->

## ⚠️ A interface roda os mesmos comandos

Se você não entende o que `git add`, `git commit` e `git push` fazem, os botões só **escondem** o problema.

O histórico de commits continua sendo o que qualquer pessoa vê ao abrir o seu repositório.

**Clique consciente.**

---

## O painel Source Control

`Ctrl+Shift+G` — ou o ícone 🔀 na barra de atividades.

Se a pasta aberta for um repositório Git, você vê:

- **Changes** — arquivos modificados. É o que o `git status` mostra;
- **Staged Changes** — os preparados para commit. É o resultado do `git add`;
- **Caixa de mensagem** no topo — a mensagem do commit.

---

<!-- _class: diagrama -->

## Do arquivo alterado ao GitHub

![w:1140](img/source-control.svg)

---

<!-- _class: tabela-densa -->

## Traduzindo botão em comando

| Na interface | Equivale a |
|---|---|
| **+** ao lado do arquivo | `git add arquivo` |
| **+** na seção Changes | `git add .` |
| **−** em Staged | `git restore --staged arquivo` |
| ↩️ **descartar** | `git restore arquivo` ⚠️ perde as alterações |
| mensagem + **Commit** | `git commit -m "mensagem"` |
| 🔄 **Sync Changes** | `git pull` seguido de `git push` |

---

## O fluxo, em seis passos

1. Edite os arquivos normalmente;
2. Abra o Source Control — `Ctrl+Shift+G`;
3. Clique no **+** dos arquivos que vão no commit;
4. Escreva uma **mensagem clara** na caixa;
5. **Commit**;
6. **Sync Changes** para enviar ao GitHub.

> 💡 A mensagem segue as mesmas boas práticas de sempre: verbo no presente, dizendo o que mudou. *"arrumei"* e *"final2"* continuam proibidos.

---

## Vendo as diferenças

Clique em qualquer arquivo modificado no painel e o VS Code abre a **visão de diff**:

- **Esquerda:** a versão do último commit;
- **Direita:** a sua versão atual;
- **Vermelho** removido · **verde** adicionado.

É o `git diff`, muito mais legível.

> 💡 **Revise o diff antes de todo commit.** É o melhor hábito que você pode criar — pega arquivo errado, `console.log` esquecido e senha colada sem querer.

---

<!-- _class: lista-limpa -->

## As marcas na margem do editor

Ao lado dos números de linha, enquanto você digita:

- 🟩 **Barra verde** — linhas adicionadas;
- 🟦 **Barra azul** — linhas modificadas;
- 🔻 **Triângulo vermelho** — linhas removidas.

Clique numa delas para ver o diff daquele trecho — e até desfazer só aquela alteração.

---

## Branches na barra de status

O canto inferior esquerdo mostra a **branch atual**.

- **Clicar no nome** abre o menu para trocar de branch ou criar uma nova — é o `git switch` / `git switch -c`;
- O **🔄 ao lado** mostra commits a enviar (↑) e a receber (↓).

---

## Clonando pelo VS Code

1. `Ctrl+Shift+P` → **Git: Clone**;
2. Cole a URL do repositório;
3. Escolha a pasta de destino;
4. **Open** quando ele perguntar.

Na primeira vez, o VS Code pede para **autenticar no GitHub** — abre o navegador e você autoriza. Depois disso, `push` e `pull` não pedem mais senha.

---

<!-- _class: lead -->

## 🔐 Em computador compartilhado

Aquela autenticação **fica salva**.

Ao terminar, deslogue:

`Ctrl+Shift+P` → `sign out` → **Accounts: Sign Out**

---

## Conflitos — onde o VS Code brilha

O arquivo abre com os marcadores que você já conhece:

```
<<<<<<< HEAD
sua versão
=======
versão que veio do remoto
>>>>>>> branch-tal
```

Mas com **botões clicáveis** acima de cada conflito: *Accept Current* · *Accept Incoming* · *Accept Both* · *Compare Changes*.

E o **Merge Editor**, em três painéis, para os casos difíceis.

---

## GitLens e Git Graph

Se você instalou as extensões do Módulo 4:

- **GitLens** — passe o cursor em qualquer linha e veja **quem** a alterou, **quando** e **em qual commit**;
- **Git Graph** — o **grafo visual** de todas as branches e commits. Ótimo para *entender* o que `merge` faz de verdade.

---

<!-- _class: checkpoint lista-limpa -->

## ✅ Checklist do módulo

- ☐ Fiz um commit completo pela interface: stage → mensagem → commit → sync;
- ☐ Sei qual comando cada botão executa;
- ☐ Revisei um diff antes de commitar;
- ☐ Troquei de branch pela barra de status;
- ☐ Clonei um repositório pelo VS Code;
- ☐ Sei deslogar do GitHub.

---

<!-- _class: lead -->

## ➡️ Próximo passo

**Módulo 7 — Configurações e Produtividade**

Deixar o editor com a sua cara —
e o último empurrão de velocidade.
