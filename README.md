# Documentação da Aplicação de venda de ingressos desenvolvida durante a imerção fullstack fullCycle 

Este projeto consiste em uma aplicação de venda de ingressos utilizando Go, NestJS, Next.js e Kong. Cada componente da aplicação está em um diretório separado. Siga as instruções abaixo para configurar e executar cada parte do projeto.

## Pré-requisitos

- Docker e Docker Compose instalados
- Node.js e npm instalados

## Passo a passo

### 1. API em Go

1. Navegue até o diretório da API Go:
    ```sh
    cd golang
    ```

2. Execute o Docker Compose:
    ```sh
    docker compose up
    ```

3. Entre no container:
    ```sh
    docker compose exec golang sh
    ```

4. No shell do container, execute o comando:
    ```sh
    go run cmd/events/main.go
    ```

### 2. API NestJS

1. Navegue até o diretório da API NestJS:
    ```sh
    cd nestjs-partners-api
    ```

2. Execute o Docker Compose:
    ```sh
    docker compose up
    ```

3. Entre no container:
    ```sh
    docker compose exec nestjs bash
    ```

4. No bash do container, execute os seguintes comandos:
    ```sh
    npm install
    npm run migrate:partner1
    npm run migrate:partner2
    npm run start partner1-fixture
    npm run start partner2-fixture
    npm run start:dev
    npm run start:dev partner2
    ```

### 3. Frontend Next.js

1. Navegue até o diretório do frontend Next.js:
    ```sh
    cd nextjs-frontend
    ```

2. Execute o Docker Compose:
    ```sh
    docker compose up
    ```

3. Entre no container:
    ```sh
    docker compose exec nextjs bash
    ```

4. No bash do container, execute os seguintes comandos:
    ```sh
    npm install
    npm run dev
    ```
    
### 4. Kong API Gateway

1. Navegue até o diretório do Kong API Gateway:
    ```sh
    cd kong-api-gateway
    ```

2. Execute o Docker Compose:
    ```sh
    docker compose up
    ```

## Conclusão

Após seguir os passos acima, você terá todos os componentes do projeto em execução. 
Certifique-se de que todos os serviços estão funcionando corretamente e interagindo 
conforme esperado. A aplicação esta rodando em: 

  ```sh
  http://localhost:8000/nextjs
  ```

