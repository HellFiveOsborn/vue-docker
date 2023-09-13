<picture>
  <img style="display:block;margin-inline:auto;" alt="VUEDOCKER" width="460" src="vuedocker.png">
</picture>

# <a href="https://vuejs.org" target="_blank" rel="noopener noreferrer"><img width="25" src="https://vuejs.org/images/logo.png" alt="Vue logo"></a>ue.js Dockerized Project

<p align="center">
  <a href="https://circleci.com/gh/vuejs/vue/tree/dev"><img src="https://img.shields.io/circleci/project/github/vuejs/vue/dev.svg?sanitize=true" alt="Build Status"></a>
  <a href="https://npmcharts.com/compare/vue?minimal=true"><img src="https://img.shields.io/npm/dm/vue.svg?sanitize=true" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/v/vue.svg?sanitize=true" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/l/vue.svg?sanitize=true" alt="License"></a>
  <a href='https://github.com/vitejs/awesome-vite'><img src='https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg' alt='Vite'></a>
</p>

Este é um projeto Vue.js que pode ser executado em um contêiner Docker para facilitar o desenvolvimento e implantação.

## Estrutura do Projeto

O projeto é organizado da seguinte forma:

```
app/
├── package.json
├── ...
├── (outros arquivos do projeto Vue.js)
└── ...
vued
Docker/Dockerfile
docker-compose.yml
```

O diretório `app/` contém o código do projeto Vue.js, incluindo o arquivo `package.json`. O script `vued` é um utilitário de linha de comando que facilita a execução das operações relacionadas ao Docker e ao projeto Vue.js.

## Comandos Disponíveis

O utilitário `vued` oferece os seguintes comandos para facilitar o desenvolvimento do projeto:

| Comando                       | Descrição                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------|
| `vued up [-d]`                | Inicia o contêiner Docker em segundo plano (use `-d` para executá-lo em segundo plano).   |
| `vued up`                     | Inicia o contêiner Docker em primeiro plano.                                              |
| `vued down`                   | Encerra o contêiner Docker.                                                               |
| `vued start <args>`        | Inicia o projeto (equivalente a `yarn start`).                                            |
| `vued dev <args>`          | Inicia o projeto como desenvolvimento (equivalente a `yarn dev`).                         |
| `vued build <args>`        | Compila o projeto (equivalente a `yarn build`).                                           |
| `vued npm <comando>`          | Executa um comando npm dentro do contêiner.                                               |
| `vued yarn <comando>`         | Executa um comando yarn dentro do contêiner.                                              |
| `vued it <bash\|sh>`           | Entra no shell do contêiner (usa `bash` como padrão, use `sh` para especificar o shell).  |
| `vued cli <comando>`          | Executa um comando Vue CLI dentro do contêiner.                                           |

## Como Usar

Siga estas etapas para iniciar o projeto em seu ambiente:

1. Clone este repositório em sua máquina local:

   ```bash
   git clone https://github.com/HellFiveOsborn/vue-docker.git
   ```
> [!IMPORTANT]
> Caso não possua um package.json em /app será criado um novo projeto automaticamente.

2. Execute o contêiner Docker:
   ```bash 
   ./vued up -d
   ```
    ```bash 
    ./vued dev <args>
    ```   
    ```bash 
    ./vued start <args>
    ```   
3. Quando terminar, você pode parar o contêiner Docker usando:
   ```bash
   ./vued down
   ```
4. Instale novos pacotes usando:
   ```bash
   ./vued <npm install|yarn add> <pacote>
   ```
5. Compile sua aplicação usando:
   ```bash
   ./vued build
   ```