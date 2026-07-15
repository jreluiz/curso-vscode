# ✏️ Exercícios Práticos

> Faça os exercícios **com o VS Code aberto**. O objetivo é criar memória muscular, não decorar.
>
> 📤 **Entrega:** crie um repositório chamado `exercicios-vscode` no seu GitHub e registre suas respostas/evidências conforme indicado em cada módulo. Capriche nas mensagens de commit!

---

## Módulo 1

**1.1** Instale o VS Code (ou localize-o no laboratório) e tire um print da tela de boas-vindas.

**1.2** Crie uma pasta chamada `exercicios-vscode` e abra-a no VS Code usando o comando `code .` no terminal do sistema.

**1.3** Dentro dela, crie um arquivo `sobre-mim.md` com: seu nome, curso e uma meta para o semestre. Salve.

**1.4** Responda em um arquivo `respostas-m1.md`:
- Qual a diferença entre um editor de código e uma IDE?
- Por que o VS Code detectou seu arquivo como Markdown?

---

## Módulo 2

**2.1** Sem usar o mouse: abra a paleta de comandos, digite `theme` e troque o tema de cores. Depois volte para o tema original.

**2.2** Usando **apenas o Explorer**, crie esta estrutura de uma vez (dica do módulo — caminho com barras!):

```
projetos/
└── js/
    └── ola.js
```

**2.3** Abra o `ola.js` com `Ctrl+P` digitando apenas parte do nome.

**2.4** Use `Ctrl+P` + `:1` para ir à linha 1. Verifique na barra de status a posição do cursor.

**2.5** Em `respostas-m2.md`, explique com suas palavras a diferença entre `Ctrl+P` e `Ctrl+Shift+P`.

---

## Módulo 3

**3.1** Cole este código em um arquivo `pratica.js`:

```javascript
let a = 1;
let b = 2;
let c = 3;
console.log(a);
console.log(b);
console.log(c);
```

Agora, **sem copiar e colar**:
- Use `Alt+↓` para mover a linha `let a = 1;` para depois de `let c = 3;`
- Use `Shift+Alt+↓` para duplicar a última linha
- Use `Ctrl+Shift+K` para excluir a duplicata

**3.2** Ainda no `pratica.js`: use `Ctrl+D` para selecionar todas as ocorrências de `console` e trocar por `console.error`. Depois desfaça tudo com `Ctrl+Z`.

**3.3** Use `F2` para renomear a variável `a` para `primeiroValor`. Observe que só as referências corretas mudaram.

**3.4** Cole um código propositalmente desalinhado (invente!) e formate com `Shift+Alt+F`.

**3.5** Ative o **Format On Save** e comprove: desalinhe o código, salve, veja a mágica.

**3.6 Desafio:** usando multicursor (`Ctrl+Alt+↓`), transforme esta lista em declarações `const`:

```
banana
maçã
uva
```

em:

```javascript
const banana = "banana";
const maçã = "maçã";
const uva = "uva";
```

---

## Módulo 4

**4.1** Instale as extensões: **Prettier**, **ESLint** e **Extension Pack for Java**. Tire um print da sua lista de extensões instaladas.

**4.2** Verifique nas páginas das extensões: quem é o publicador de cada uma? Todos têm o selo de verificado?

**4.3** Instale o **Live Server**, crie um `index.html` (use `!` + `Tab` para gerar a estrutura!) e abra com *Go Live*. Edite o `<h1>` e veja o navegador atualizar sozinho.

**4.4** Configure o Prettier como formatador padrão e comprove que um arquivo `.js` bagunçado é formatado ao salvar.

**4.5** Em `respostas-m4.md`: cite 3 critérios para avaliar se uma extensão é confiável e explique por que isso importa.

---

## Módulo 5

**5.1** Abra o terminal integrado e execute: `pwd`, `ls` e crie uma pasta `teste-terminal` com `mkdir`.

**5.2** Crie um arquivo `contador.js`:

```javascript
for (let i = 1; i <= 5; i++) {
  console.log(`Contando: ${i}`);
}
```

Execute com `node contador.js`. Cole a saída em `respostas-m5.md`.

**5.3** Modifique o loop para ser **infinito** (`while (true)` imprimindo algo), execute e **interrompa com `Ctrl+C`**. Anote o que aconteceu.

**5.4** (Java) Crie uma classe `Ola.java` com um `main` que imprime seu nome. Execute **das duas formas**: pelo botão Run e compilando manualmente com `javac`/`java` no terminal.

**5.5** Abra **dois terminais lado a lado** (botão de dividir). Em `respostas-m5.md`, descreva uma situação em que isso seria útil.

---

## Módulo 6

> Estes exercícios usam o repositório `exercicios-vscode` que você vem construindo.

**6.1** Se ainda não fez: `git init` no repositório, conecte ao GitHub e faça o primeiro push.

**6.2** Modifique dois arquivos diferentes. No painel Source Control:
- Faça **stage de apenas um** deles
- Commite com uma mensagem adequada
- Depois commite o segundo separadamente
- Em `respostas-m6.md`, explique por que commits separados fazem sentido aqui

**6.3** Antes do próximo commit, clique no arquivo modificado e **analise o diff**. Tire um print da visão de comparação.

**6.4** Pela **barra de status**, crie uma branch `exercicio-branch`, faça um commit nela, volte para a `main` e observe o arquivo "desaparecer" e "reaparecer" ao trocar de branch.

**6.5** Faça o **Sync Changes** e confirme no GitHub (pelo navegador) que os commits chegaram.

**6.6 Desafio (em dupla):** provoquem um **conflito de merge** de propósito (os dois editam a mesma linha do mesmo arquivo em branches diferentes) e resolvam usando os botões do VS Code. Documentem o processo com prints em `conflito-resolvido.md`.

---

## Módulo 7

**7.1** Configure seu `settings.json` (User) com pelo menos 4 das configurações recomendadas no módulo. Cole seu JSON em `respostas-m7.md`.

**7.2** Em um arquivo HTML, use Emmet para gerar:
- A estrutura HTML5 (`!`)
- Uma `div.container` contendo uma `ul` com 5 `li`
- Anote as abreviações que usou.

**7.3** Crie um snippet pessoal para algo que você digita com frequência (sugestão: um cabeçalho de comentário com seu nome e data). Demonstre-o funcionando.

**7.4** No `contador.js` do Módulo 5: coloque um **breakpoint** dentro do loop, execute com `F5` e avance com `F10` observando o valor de `i` mudar no painel de variáveis. Tire um print com a execução pausada.

**7.5 Desafio final:** crie um `.vscode/settings.json` **dentro do repositório** `exercicios-vscode` com configurações de workspace, commite e faça push. Verifique no GitHub que a pasta `.vscode` está lá — agora qualquer pessoa que clonar seu projeto herda suas configurações!

---

## 🏁 Entrega final

Ao concluir todos os módulos, seu repositório `exercicios-vscode` deve ter:

- [ ] Todos os arquivos de resposta (`respostas-m1.md` a `respostas-m7.md`)
- [ ] Histórico de commits **limpo e descritivo** (será avaliado!)
- [ ] Pelo menos uma branch além da `main` no histórico
- [ ] O arquivo `.vscode/settings.json` versionado

[← Voltar ao índice](../README.md)
