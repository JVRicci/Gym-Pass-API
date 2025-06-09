# Inicio da aplicação

Inicialmente na API forma instaladas as libs para começar o projeto

```bash
     npm i typescript @types/node tsx tsup -D
```

Para criar o tsconfig 

```bash
     npx tsc --init
```

A versão do ecmascript utilizada é a 2020, como foi configurada no tsconfig
Após isso, foi instalado o Fastify como microframework para desenvolvimento da API

```bash
    npm i fastify
```

# Arquivo .npmrc

O arquivo serve para que as versões das dependencias instaladas não se alterem, ou seja, fiquem fixas
Após criar esse arquivo com o comando 

```js
    save-exact=true
```

Basta apenas instalar novamente as dependencias

# Variáveis de ambiente

Para o projeto é utilizada a lib dotenv para verificação de variáveis de ambiente

```bash
    npm i dotenv
```

# Validacão de variáveis

Para o projeto é utilizada a lib zod para verificação de variáveis 

```bash
    npm i zod
```