# 🔧 Troubleshooting — Problemas Comuns e Soluções

> Antes de qualquer coisa: **feche e reabra o VS Code**. Resolve mais do que parece. 😄
> Segundo recurso universal: `Ctrl+Shift+P` → **Developer: Reload Window** (recarrega sem fechar).

---

## 🚫 "O comando `code .` não funciona no terminal"

**Sintoma:** `'code' não é reconhecido como um comando...`

**Causa:** o VS Code não foi adicionado ao PATH na instalação.

**Solução:**
- **Windows:** reinstale marcando a opção *"Adicionar ao PATH"*, ou adicione manualmente a pasta `C:\Users\SEU-USUARIO\AppData\Local\Programs\Microsoft VS Code\bin` às variáveis de ambiente
- **macOS:** `Cmd+Shift+P` → *Shell Command: Install 'code' command in PATH*
- Em qualquer caso: **feche e reabra o terminal** depois

---

## 🚫 "Digitei `node arquivo.js` e deu 'node não é reconhecido'"

**Causa:** o Node.js não está instalado ou não está no PATH.

**Solução:**
1. Baixe e instale o Node.js LTS em https://nodejs.org
2. **Feche e reabra o VS Code** (o terminal integrado herda o PATH de quando o VS Code abriu!)
3. Teste: `node --version`

> 💡 Esse detalhe pega muita gente: se você instalou o Node **com o VS Code aberto**, o terminal integrado ainda não "enxerga" a instalação. Reiniciar o VS Code resolve.

---

## 🚫 "O código Java não compila / a extensão reclama de JDK"

**Sintoma:** aviso como *"Java runtime could not be located"*.

**Solução:**
1. Instale um **JDK 17 ou superior** (Adoptium/Temurin é uma boa opção gratuita: https://adoptium.net)
2. Reinicie o VS Code
3. Se persistir: `Ctrl+Shift+P` → **Java: Configure Java Runtime** e verifique se o JDK aparece

---

## 🚫 "O IntelliSense parou de funcionar / sugestões não aparecem"

**Soluções em ordem:**
1. `Ctrl+Espaço` para forçar as sugestões
2. Verifique na **barra de status** se a linguagem foi detectada corretamente (canto inferior direito)
3. `Ctrl+Shift+P` → **Developer: Reload Window**
4. Para Java: `Ctrl+Shift+P` → **Java: Clean Java Language Server Workspace**

---

## 🚫 "O Prettier não formata ao salvar"

**Checklist:**
1. A extensão **Prettier** está instalada e habilitada?
2. `Ctrl+,` → busque `format on save` → está marcado?
3. `Ctrl+,` → busque `default formatter` → está como **Prettier - Code formatter**?
4. Teste manualmente com `Shift+Alt+F` — se aparecer *"There are multiple formatters..."*, escolha o Prettier e marque para lembrar

---

## 🚫 "Os arquivos não aparecem coloridos no painel do Git / o Source Control diz que não há repositório"

**Causas possíveis:**
- A pasta aberta **não é** um repositório Git → rode `git init` no terminal
- Você abriu um **arquivo solto** em vez da **pasta do projeto** → `File → Open Folder`
- O Git não está instalado na máquina → `git --version` para verificar

---

## 🚫 "O VS Code pede login no GitHub toda hora / push falha com erro de autenticação"

**Soluções:**
1. `Ctrl+Shift+P` → digite `sign in` → **Accounts** → entre com o GitHub
2. Se as credenciais ficaram "presas" de outro usuário (comum no laboratório!):
   - Windows: abra o **Gerenciador de Credenciais** → Credenciais do Windows → remova as entradas `git:https://github.com`
   - Depois tente o push de novo — o VS Code pedirá o login correto

> 🔐 **No laboratório:** sempre desconecte sua conta ao final (`Ctrl+Shift+P` → *Sign Out*) e confira o Gerenciador de Credenciais.

---

## 🚫 "Aparecem mil erros vermelhos em um projeto que estava funcionando"

**Causas comuns:**
- **Dependências não instaladas** (JS): rode `npm install` no terminal — a pasta `node_modules` não vai para o Git (está no `.gitignore`), então após clonar é preciso instalar
- **Workspace Java corrompido:** `Ctrl+Shift+P` → **Java: Clean Java Language Server Workspace** → *Reload and delete*

---

## 🚫 "O terminal abre com o shell errado (quero Git Bash / PowerShell)"

`Ctrl+Shift+P` → **Terminal: Select Default Profile** → escolha o shell desejado → abra um **novo** terminal (o botão +).

---

## 🚫 "Fechei uma aba/painel e não sei como trazer de volta"

- Aba de arquivo: `Ctrl+Shift+T`
- Barra lateral: `Ctrl+B`
- Painel/terminal: `Ctrl+J`
- Qualquer visão: menu `View` ou `Ctrl+Shift+P` e digite o nome dela

---

## 🚫 "O VS Code está lento"

**Suspeitos de sempre:**
1. **Extensões demais** — desative as que não usa (`Ctrl+Shift+X` → engrenagem → *Disable*)
2. `Ctrl+Shift+P` → **Developer: Show Running Extensions** mostra quanto cada extensão consome
3. Pastas gigantes abertas (ex.: abriu o disco inteiro em vez da pasta do projeto)
4. `node_modules` sendo vasculhado pela busca — normalmente já é ignorado por padrão

---

## 🚫 "Deletei um trecho de código importante e já salvei!"

Calma, há camadas de proteção:

1. `Ctrl+Z` — se o arquivo ainda está aberto
2. **Timeline** — Explorer → painel *Timeline* na parte de baixo → histórico local do arquivo
3. **Git** — se o trecho estava commitado: painel Source Control → clique no arquivo → compare e restaure
4. Aprendeu a lição? Commits pequenos e frequentes! 😄

---

## ❓ Não achou seu problema aqui?

1. Copie a **mensagem de erro exata** e pesquise
2. Consulte a documentação oficial: https://code.visualstudio.com/docs
3. Abra uma **Issue** neste repositório descrevendo o problema (ótima prática de colaboração!)

[← Voltar ao índice](README.md)
