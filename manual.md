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

# ESLint

O projeto utiliza ESlint como formatador de código

```bash
    npm i eslint -D
```

Para iniciar 

```bash
    npx eslint --init
```

# Configurando path 

No arquivo tsconfig foram editadas as seguintes linhas

```js
    "baseUrl": "./",
    "paths": {
      "@/*" : ["./src/*"]
    }, 
```

# Query Builder vs ORM

No projeto é utilizada a ORM Prisma
A diferença entre ORM e Query Builders se dá no nivel de abstração: Enquanto os Query Builders são focados em preparar queries para o banco, sem ter controle direto sobre a estrutura do banco (tabelas, schemas, etc), os ORM fazem também esse serviço, manipulando tabelas do banco, em criaçoes e alterações por exemplo e dessa forma, mapeando o banco de dados na aplicação

Para instalação do prisma:

```bash
    npm i prisma - D
```

Para iniciar o ORM e banco

```bash
    npx primas init
```

Com isso será criada a pasta prisma e nela o arquivo schema

Após isso é possivel criar models no arquivo schema.prisma
Com as models criadas, basta apenas usar o seguinte comando para gerar as tabelas

```bash
    npx prisma generate
```

Para fazer queries é necessário o pacote 

```bash
    npm i @prisma/client
```