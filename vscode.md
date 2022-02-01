# Instalando e configurando o Visual Studio Code

Para instalar o editor de texto Visual Studio Code em qualquer um dos 3 sistemas operacionais, basta [acessar o site](https://code.visualstudio.com/), baixar e rodar o executável.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9dddb31-2111-4767-9e21-2c3f5f5fc85a/vscode.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9dddb31-2111-4767-9e21-2c3f5f5fc85a/vscode.gif)

Com a instalação finalizada, abra o programa. Você deve se deparar com uma interface parecida com essa:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bf9ea041-d406-47c3-848e-18c53e9605e7/1-welcome.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bf9ea041-d406-47c3-848e-18c53e9605e7/1-welcome.png)

Feche a página **Welcome**. Para deixar a sua experiência ainda melhor, vamos passar para você algumas extensões e configurações do VS Code.

## Fonte

Essa não é uma etapa obrigatória, mas se você quer uma fonte mais personalizada e com todos aqueles símbolos especiais quando combinamos alguns caracteres, basta seguir alguns passos:

### JetBrains Mono

- A fonte utilizada nas aulas se chama JetBrains Mono e pode ser baixada gratuitamente no site da JetBrains através do seguinte link:

[JetBrains Mono: A free and open source typeface for developers](https://www.jetbrains.com/lp/mono/)

1 - Após baixar, extraia o arquivo e acesse a pasta `ttf`.

2 - Para instalar a fonte:

- **Windows**
    
    Selecione todos os arquivos que terminam com **.ttf**, clique com o botão direito do mouse e selecione **Instalar**.
    
- **Linux**
    
    Extraia as fontes para `~/.local/share/fonts` ou `/usr/share/fonts` para instalar as fontes no sistema e execute `fc-cache -f -v` no terminal.
    
- **Mac**
    
    Selecione todos os arquivos de fontes (aqueles que possuem a extensão **.ttf**), dê um duplo clique neles e clique no botão **Instalar Fonte**.
    

3 - O próximo passo é configurar a fonte para ser usada no Visual Studio Code. Após ter realizado as demais instalações, você poderá encontrar as configurações da fonte na seção **[Configurações](https://www.notion.so/Instala-o-das-ferramentas-2e3f74b481204a69a1189a4cfe54adc7)**.

### Usando as Font Ligatures

Uma das características dessa fonte é que ela possui suporte às font ligatures que é uma funcionalidade que permite combinarmos símbolos para formar um novo.

Aqui você verá como são formados os símbolos mais comuns usados durante a NLW para que não fique confuso quando ver algo diferente:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9d8c2af-1b3c-410b-b359-825ca02e1de2/fontLigatures.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9d8c2af-1b3c-410b-b359-825ca02e1de2/fontLigatures.png)

## Extensões

Extensões são formas de adicionar ainda mais funcionalidades ao seu Visual Studio Code.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b296ac36-a8dd-4117-a1e0-b7999e1990ea/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b296ac36-a8dd-4117-a1e0-b7999e1990ea/Untitled.png)

Vamos citar 2 aqui para você:

### Omni

Nada melhor do que começar pelo tema do editor. Nós desenvolvedores trabalhamos diariamente, horas e horas, com o editor de código. Por isso, é muito importante escolher uma aparência para o Visual Studio Code que não canse demais os olhos e ao mesmo tempo realce bem o texto. É por isso que a Rocketseat decidiu criar (baseado no nosso querido Dracula) o seu próprio tema: Omni

**Como instalar? ⬇️**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/76bd3f8f-1b2c-4ec4-bd6d-b92270cabd24/omni.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/76bd3f8f-1b2c-4ec4-bd6d-b92270cabd24/omni.gif)

### Material Icon Theme

O **Material Icon Theme** é uma extensão que permite a customização dos ícones das pastas por extensões de arquivos, por exemplo, com ele conseguimos customizar um ícone para arquivos **Typescript**, outro para **Javascript,** outro para **HTML** e assim por diante. 

**Como instalar? ⬇️**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f235cd7c-7840-4e60-8d4e-81643dfe0895/materialicone.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f235cd7c-7840-4e60-8d4e-81643dfe0895/materialicone.gif)

## Configurações

Para finalizar, vamos adicionar algumas configurações no Visual Studio Code. Para isso, basta pressionar `Ctrl + Shift + P` e escolher a opção `Open Settings (JSON)`. Na janela que foi aberta, adicione as configurações abaixo:

## Configurações do Vscode
```bash
"terminal.integrated.fontSize": 14,

"editor.tabSize": 2,
"editor.fontSize": 16,
"editor.lineHeight": 26,
"editor.semanticHighlighting.enabled": false,

"editor.rulers": [80, 120],

"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
},

"files.exclude": {
  "**/.git": true,
  "**/.svn": true,
  "**/.hg": true,
  "**/CVS": true,
  "**/.DS_Store": true,
  // "**/node_modules": true
},

"files.associations": {
  ".sequelizerc": "javascript",
  ".stylelintrc": "json",
  ".prettierrc": "json",
  "*.tsx": "typescriptreact"
},

"typescript.tsserver.log": "verbose",
"material-icon-theme.activeIconPack": "nest",

"material-icon-theme.folders.associations": {
  "infra": "app",
  "entities": "class",
  "domain": "class",
  "schemas": "class",
  "typeorm": "database",
  "repositories": "mappings",
  "http": "container",
  "migrations": "tools",
  "modules": "components",
  "implementations": "core",
  "dtos": "typescript",
  "fakes": "mock",
  "websockets": "pipe",
  "protos": "pipe",
  "grpc": "pipe",
  "providers": "include",
  "subscribers": "messages",
  "useCases": "controller",
  "kafka": "scripts",
  "mappers": "meta",
  "_shared": "shared",
  "eslint-config": "tools",
  "kube": "kubernetes"
},

"material-icon-theme.files.associations": {
  "ormconfig.json": "database",
  "tsconfig.json": "tune",
  "*.proto": "3d",
  "*.webpack.js": "webpack"
},
"window.menuBarVisibility": "toggle",
"tabnine.experimentalAutoImports": true,
"cSpell.enableFiletypes": [
  "!asciidoc",
  "!c",
  "!cpp",
  "!csharp",
  "!go",
  "!handlebars",
  "!haskell",
  "!jade",
  "!java",
  "!latex",
  "!php",
  "!pug",
  "!python",
  "!restructuredtext",
  "!rust",
  "!scala",
  "!scss"
],
"cSpell.language": "en,pt",
"editor.suggestSelection": "first",
"cSpell.userWords": [
  "chakra",
  "middlewares",
  "prefetch",
  "rocketseat"
],
"workbench.productIconTheme": "fluent-icons",
"terminal.integrated.showExitAlert": false,

"splitHTMLAttributes.closingBracketOnNewLine": true,
"window.zoomLevel": 1
```