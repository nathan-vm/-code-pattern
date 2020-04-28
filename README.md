# Code pattern

- [ ]  Instalar VSCode
- [ ]  Instalar NodeJS 12.x
- [ ]  Instalar yarn (opcional)
- [ ]  Instalar extensão ESLint no vscode
- [ ]  Instalar extensão Editor Config no vscode

# Iniciar projeto (node ou react)

exemplo com projeto node:

```bash
npm --init
```

```bash
yarn --init
```

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-14-26.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-14-26.png)

### Instalar eslint no projeto

```bash
npm install eslint --save-dev
```

```bash
yarn add eslint -D
```

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-15-32.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-15-32.png)

### Configurar ESLint

```bash
yarn eslint --init
```

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-15-58.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-15-58.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-02.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-02.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-07.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-07.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-11.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-11.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-19.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-19.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-23.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-23.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-27.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-27.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-31.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-31.png)

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-37.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-16-37.png)

Instale as dependencias necessárias utilizando o gerenciador de pacotes de sua escolha, se estiver utilizando o npm pode marcar com "y" a ultima pergunta e a instalação seguirá, ou se for como o meu caso copiei as dependencias e instale retirando os ">=" e substituindo por "^"

Exemplo:

```bash
yarn add -D eslint-config-standard@latest eslint@^6.2.2 eslint-plugin-import@^2.18.0 eslint-plugin-node@^9.1.0 eslint-plugin-promise@^4.2.1 eslint-plugin-standard@^4.0.0
```

### Instalar Prettier:

```bash
yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
```

```bash
npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
```

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-19-04.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-19-04.png)

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

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-20-10.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-20-10.png)

### Configurar o editorconfig para evitar incompatibilidade de formatação

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-20-28.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-20-28.png)

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

![Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-21-02.png](Tutorial%20ESLint%20Prettier/Captura_de_tela_de_2020-04-28_18-21-02.png)
