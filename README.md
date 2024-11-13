# Iniciando o projeto

```sh
npm install -D typescript @types/node ts-node nodemon
```

## Criação arquivo `tsconfig.json`


Crie um arquivo na raiz do projeto com o nome `tsconfig.json` com o conteúdo abaixo:

```json
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}
```

## Configuração arquivo `.gitignore`

Crie um arquivo na raiz do projeto com o nome `.gitignore` com o conteúdo abaixo:

```
node_modules
dist
```

## Configuração arquivo `package.json`

Dentro do arquivo `package.json`, apague o script de teste e coloque os seguintes scripts:

```json
  "scripts": {
    "dev": "nodemon ./src/index.ts",
    "start": "npx tsc && node ./dist/index.js"
  },
```