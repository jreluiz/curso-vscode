# Módulo 7 — Configurações e Produtividade

[← Módulo anterior](06-git-github-no-vscode.md) | [Voltar ao índice](README.md)

---

## 7.1 O sistema de configurações

Abra as configurações com `Ctrl+,` (Control + vírgula). Há duas visões:

- **Interface gráfica** — busca e caixinhas, ótima para descobrir opções
- **JSON** — `Ctrl+Shift+P` → _Open User Settings (JSON)_ — edição direta, ótima para copiar configurações prontas

### User vs. Workspace

| Escopo        | Onde fica                                   | Vale para                                   |
| ------------- | ------------------------------------------- | ------------------------------------------- |
| **User**      | Perfil do usuário no sistema                | **Todos** os seus projetos                  |
| **Workspace** | `.vscode/settings.json` na pasta do projeto | **Só aquele projeto** (e vai junto no Git!) |

> 💡 **Dica de equipe:** projetos costumam incluir um `.vscode/settings.json` com configurações padronizadas — todo mundo com a mesma formatação facilita a revisão dos Pull Requests.

### Configurações recomendadas para começar

```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": false,
  "files.autoSave": "onFocusChange",
  "editor.linkedEditing": true,
  "explorer.confirmDelete": true
}
```

O que cada uma faz:

- `formatOnSave` — formata ao salvar (viu no Módulo 3)
- `tabSize: 2` — indentação de 2 espaços (padrão da comunidade JS; para Java, 4 é comum)
- `wordWrap` — quebra linhas longas visualmente (sem alterar o arquivo)
- `autoSave: onFocusChange` — salva ao trocar de janela/aba (adeus, "esqueci de salvar"!)
- `linkedEditing` — em HTML, editar a tag de abertura edita a de fechamento junto

## 7.2 Temas e aparência

- `Ctrl+K Ctrl+T` — troca o **tema de cores** rapidamente
- Zoom da interface: `Ctrl+=` / `Ctrl+-` (útil para projetar na aula!)
- Tamanho da fonte do editor: busque `font size` nas configurações

## 7.3 Emmet — HTML e CSS em alta velocidade

O **Emmet** vem embutido no VS Code e expande abreviações em código HTML/CSS. Digite a abreviação e pressione `Tab`:

| Você digita              | Vira                       |
| ------------------------ | -------------------------- |
| `!`                      | Estrutura HTML5 completa   |
| `div.card`               | `<div class="card"></div>` |
| `ul>li*3`                | Lista com 3 itens          |
| `h1{Olá}`                | `<h1>Olá</h1>`             |
| `.container>.row>.col*2` | Estrutura aninhada de divs |

> 💡 Muito útil ao trabalhar com HTML e páginas web.

## 7.4 Snippets — seus próprios atalhos de código

Snippets são **modelos de código** que se expandem. O VS Code já vem com vários (digite `for` em um `.js` e veja as sugestões), e você pode criar os seus:

1. `Ctrl+Shift+P` → **Snippets: Configure Snippets**
2. Escolha a linguagem (ex.: `javascript`)
3. Adicione, por exemplo:

```json
{
  "Console log rápido": {
    "prefix": "cl",
    "body": "console.log($1);",
    "description": "Atalho para console.log"
  }
}
```

Agora, digitar `cl` + `Tab` gera `console.log()` com o cursor já dentro dos parênteses. O `$1` marca onde o cursor para.

## 7.5 Depuração básica (debugger)

O `console.log` é útil, mas o **debugger** é profissional. Introdução rápida:

1. Clique na **margem esquerda** de uma linha para criar um **breakpoint** (bolinha vermelha)
2. Pressione `F5` (em um `.js`, escolha **Node.js**; em Java, a extensão já cuida de tudo)
3. A execução **pausa** no breakpoint. Agora você pode:
   - Inspecionar o valor de **todas as variáveis** (painel à esquerda)
   - `F10` — executar a próxima linha (_step over_)
   - `F11` — entrar dentro da função (_step into_)
   - `F5` — continuar até o próximo breakpoint

> 📚 Depuração é uma habilidade avaliada tão importante quanto escrever código.

## 7.6 Dicas finais de produtividade

- **`Ctrl+K Ctrl+S`** — abre a lista de **todos os atalhos** (e permite personalizá-los)
- **Reabrir aba fechada:** `Ctrl+Shift+T` (igual ao navegador!)
- **Abrir a mesma pasta em nova janela:** útil com dois monitores
- **Perfis:** o VS Code permite criar perfis com conjuntos diferentes de extensões e configurações (ex.: um perfil "Java", um "Web") — `Ctrl+Shift+P` → _Profiles_
- **Sincronização de configurações:** com a conta GitHub, o _Settings Sync_ leva suas configurações e extensões para qualquer máquina — ⚠️ evite ativar em computadores compartilhados do laboratório

---

## 🎓 Conclusão do curso

Você agora domina o essencial do VS Code! O caminho a partir daqui:

1. **Use os atalhos** até virarem automáticos (o [cheatsheet](CHEATSHEET.md) ajuda)
2. **Explore** a paleta de comandos quando tiver dúvida — quase tudo está lá
3. **Consulte** o [guia de troubleshooting](TROUBLESHOOTING.md) quando algo der errado

## ✅ Checklist do módulo

- [ ] Configurei o `settings.json` com as opções recomendadas
- [ ] Testei o Emmet em um arquivo HTML
- [ ] Criei um snippet próprio
- [ ] Executei um programa com breakpoint e inspecionei variáveis

## ✏️ Exercícios

Faça os [exercícios do Módulo 7](exercicios/README.md#módulo-7).

---

[← Módulo anterior](06-git-github-no-vscode.md) | [Voltar ao índice](README.md)
