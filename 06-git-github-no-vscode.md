# Módulo 6 — Git e GitHub no VS Code

[← Módulo anterior](05-terminal-integrado.md) | [Voltar ao índice](README.md) | [Próximo módulo →](07-configuracoes-produtividade.md)

---

> 📚 **Pré-requisito:** este módulo assume que você já conhece o básico de Git e GitHub (add, commit, push, pull). Aqui vamos ver como o VS Code **facilita** o que você já sabe fazer no terminal — sem substituir o entendimento dos comandos!

## 6.1 A filosofia: interface ajuda, mas o terminal ensina

O VS Code tem uma integração excelente com o Git. Mas atenção:

> ⚠️ **A interface gráfica executa os mesmos comandos que você aprendeu.** Se você não entende o que `git add`, `git commit` e `git push` fazem, os botões só vão esconder o problema. Nas avaliações, o histórico de commits continua sendo analisado — clique consciente! 😄

## 6.2 O painel Source Control

Clique no ícone 🔀 na barra de atividades (ou `Ctrl+Shift+G`). Se a pasta aberta for um repositório Git, você verá:

- **Changes** — arquivos modificados (equivalente ao que `git status` mostra)
- **Staged Changes** — arquivos preparados para commit (o resultado do `git add`)
- Uma **caixa de mensagem** no topo — a mensagem do commit

### Traduzindo botões em comandos

| Ação na interface | Comando equivalente |
|-------------------|---------------------|
| Botão **+** ao lado do arquivo | `git add arquivo` |
| Botão **+** na seção Changes | `git add .` |
| Botão **−** (em Staged) | `git restore --staged arquivo` |
| Ícone de **descartar** (↩️) | `git restore arquivo` ⚠️ perde as alterações! |
| Escrever mensagem + **Commit** | `git commit -m "mensagem"` |
| Botão **Sync Changes** 🔄 | `git pull` seguido de `git push` |
| **...** → Push / Pull | `git push` / `git pull` |

### Fluxo básico pelo VS Code

1. Edite seus arquivos normalmente
2. Abra o Source Control (`Ctrl+Shift+G`) — os arquivos alterados aparecem em **Changes**
3. Clique no **+** dos arquivos que quer commitar (stage)
4. Escreva uma **mensagem de commit clara** na caixa de texto
5. Clique em **Commit**
6. Clique em **Sync Changes** para enviar ao GitHub

> 💡 **Boa prática:** mensagens de commit seguem boas práticas — verbo no imperativo, descrição clara do *quê* e *por quê*. "arrumei" e "final2" seguem proibidos! 😉

## 6.3 Vendo as diferenças (diff)

Clique em qualquer arquivo modificado no painel Source Control e o VS Code abre a **visão de diff**:

- **Esquerda:** versão do último commit
- **Direita:** sua versão atual
- Vermelho = removido, verde = adicionado

Isso equivale ao `git diff`, mas muito mais legível. **Revise o diff antes de todo commit** — é o melhor hábito que você pode criar.

### Indicadores na margem do editor

Repare nas **marcas coloridas** na margem esquerda do editor, ao lado dos números de linha:

- **Barra verde** — linhas adicionadas
- **Barra azul** — linhas modificadas
- **Triângulo vermelho** — linhas removidas

Clique nelas para ver o diff daquele trecho e até **desfazer** a alteração pontual.

## 6.4 Branches na barra de status

No canto inferior esquerdo, a barra de status mostra a **branch atual** (ex.: `main`).

- **Clicar no nome da branch** abre um menu para trocar de branch ou criar uma nova (equivalente a `git switch` / `git switch -c`)
- O ícone 🔄 ao lado mostra commits a enviar (↑) e a receber (↓)

## 6.5 Clonando um repositório pelo VS Code

Para clonar um repositório:

1. `Ctrl+Shift+P` → **Git: Clone**
2. Cole a URL do repositório (ex.: `https://github.com/SEU-USUARIO/projeto-js.git`)
3. Escolha a pasta de destino
4. Clique em **Open** quando o VS Code perguntar

Na primeira vez, o VS Code pedirá para **autenticar no GitHub** — uma janela do navegador abre e você autoriza. Depois disso, push e pull funcionam sem pedir senha.

> 🔐 **No laboratório:** lembre-se de **deslogar do GitHub ao final da aula**! `Ctrl+Shift+P` → digite `sign out` → **Accounts: Sign Out**. Também é possível verificar as contas conectadas no ícone 👤 no canto inferior esquerdo.

## 6.6 Resolvendo conflitos de merge no VS Code

Aqui o VS Code brilha. Quando um `pull` ou `merge` gera conflito, o arquivo abre com os marcadores que você conhece:

```
<<<<<<< HEAD
sua versão
=======
versão que veio do remoto
>>>>>>> branch-tal
```

Mas o VS Code adiciona **botões clicáveis** acima de cada conflito:

- **Accept Current Change** — mantém a sua versão
- **Accept Incoming Change** — aceita a versão que chegou
- **Accept Both Changes** — mantém as duas
- **Compare Changes** — mostra lado a lado

Há também o **Merge Editor** (visual em 3 painéis), ativado pelo botão *Resolve in Merge Editor*.

> 📚 **Na prática:** em qualquer projeto colaborativo, conflitos vão acontecer — é normal e esperado. Dominar este módulo é o seu kit de sobrevivência.

## 6.7 GitLens e Git Graph (extensões do Módulo 4)

Se você instalou as extensões recomendadas:

- **GitLens** — passe o cursor em qualquer linha e veja **quem** a alterou, **quando** e **em qual commit** (o famoso `git blame`, humanizado)
- **Git Graph** — clique em *Git Graph* na barra de status e veja o **grafo visual** de todas as branches e commits — ótimo para *entender* o que `merge` e `rebase` fazem

---

## ✅ Checklist do módulo

- [ ] Fiz um commit completo pela interface (stage → mensagem → commit → sync)
- [ ] Sei qual comando cada botão executa
- [ ] Revisei um diff antes de commitar
- [ ] Troquei de branch pela barra de status
- [ ] Clonei um repositório pelo VS Code
- [ ] Sei deslogar do GitHub no laboratório

## ✏️ Exercícios

Faça os [exercícios do Módulo 6](exercicios/README.md#módulo-6).

---

[← Módulo anterior](05-terminal-integrado.md) | [Voltar ao índice](README.md) | [Próximo módulo →](07-configuracoes-produtividade.md)
