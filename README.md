# Code pattern

- [ ]  Instalar [VSCode](https://code.visualstudio.com/download "download VSCode")
- [ ]  Instalar [NodeJS](https://nodejs.org/en/ "NodeJS download") 12.x
- [ ]  Instalar [yarn](https://yarnpkg.com/getting-started/install "Gloabal Install") (opcional recomendado)
- [ ]  Instalar extensão [ESLint](#eslint-extension) no vscode
- [ ]  Instalar extensão [EditorConfig](#editorconfig-extension) no vscode
- [ ]  [Configure](#Configurações-do-VSCode) o VSCode !!!


###### Para abrir o terminal dentro do VSCode clique em View -> Terminal ou teclas de atalho (Ctrl Shift `)

#### PARA ESSE TUTORIAL UTILIZE NPM _OU_ YARN


# Iniciar projeto (node ou react)

exemplo com projeto node:

```bash
npm --init
```

```bash
yarn --init
```

![Imgur](https://i.imgur.com/tq1h9ck.png)

### Instalar eslint no projeto

```bash
npm install eslint --save-dev
```

```bash
yarn add eslint -D
```

![Imgur](https://i.imgur.com/ZqAHf3v.png)

### Configurar ESLint

```bash
yarn eslint --init
```

![Imgur](https://i.imgur.com/7aAvm8g.png)

![Imgur](https://i.imgur.com/23Pvj4f.png)

![Imgur](https://i.imgur.com/8OPHK0u.png)

![Imgur](https://i.imgur.com/A2lEfjf.png)

![Imgur](https://i.imgur.com/5BWR6sl.png)

![Imgur](https://i.imgur.com/bbabVOv.png)

![Imgur](https://i.imgur.com/nAYw0u5.png)

![Imgur](https://i.imgur.com/qcK5Cu8.png)

![Imgur](https://i.imgur.com/uvKePlB.png)

Instale as dependencias necessárias utilizando o [gerenciador de pacotes](https://pt.wikipedia.org/wiki/Sistema_gestor_de_pacotes "O que é um gerenciador de pacotes?") de sua escolha, se estiver utilizando o npm pode marcar com "y" a ultima pergunta e a instalação seguirá, ou se for como o meu caso copiei as dependencias e instale retirando os ">=" e substituindo por "^"

Exemplo:

```bash
yarn add -D eslint-config-standard@latest eslint@^6.2.2 eslint-plugin-import@^2.18.0 eslint-plugin-node@^9.1.0 eslint-plugin-promise@^4.2.1 eslint-plugin-standard@^4.0.0
```
![Imgur](https://i.imgur.com/6J8uldp.png)

### Instalar Prettier:

```bash
yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
```

```bash
npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
```

![Imgur](https://i.imgur.com/2O3eLD1.png)

```json
"extends": [
    "standard",
    "plugin:prettier/recommended"
],
"plugins": [
    "prettier"
],
"rules": {
    "prettier/prettier":[
        "error",
        {
            "singleQuote": true,
            "semi": false,
            "trailingComma": "all",
            "arrowParens": "avoid"
        }
    ]
}
```

![Imgur](https://i.imgur.com/XTiQF2Y.png)

### Configurar o editorconfig para evitar incompatibilidade de formatação

![Imgur](https://i.imgur.com/NFFj60F.png)

```json
root = true

[*]
end_of_line = lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

![Imgur](https://i.imgur.com/q4TP7kO.png)



# Configurações-do-VSCode

###### Clique em Files -> Preferences -> settings e em seguida busque pelo icone demonstrado na imagem abaixo

![Imgur](https://i.imgur.com/0qRm1J3.png)

Em seguida adicione as seguintes configurações :
```
    "[javascript]":{
      "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
      }
    },
    "[javascriptreact]":{
      "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
      }
    },
    "[typescript]":{
      "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
      }
    },
    "[typescriptreact]":{
      "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
      }
    },

    "files.associations": {
      ".sequelizerc":"javascript",
      ".stylelintrc":"json",
      ".prettierrc":"json",
    }
```

![Imgur](https://i.imgur.com/iMR9sA9.png)


# eslint-extension
Na barra lateral esquerda do VSCode clique no icone de extensões e busque por ESlint
![Imgur](https://i.imgur.com/QhRhfbi.png)
# editorconfig-extension
Na barra lateral esquerda do VSCode clique no icone de extensões e busque por EditorConfig
![Imgur](https://i.imgur.com/tEBplch.png)
