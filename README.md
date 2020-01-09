# PDisc

O projeto PDisc é uma aplicão web para catálogo de discos musicais.

## PDisc-dev-env 
O objetivo desse repositório é configurar o ambiente de desenvolvimento do projeto PDisc.

## Dependências

- Docker v18.09.6 +
- Docker-compose v1.24.1 +

## Instalação

Siga os passos a seguir para configurar o ambiente do PDisc em sua máquina:

### 1. Clone este repositório

```shell
git clone https://github.com/victorhmf/PDisc-dev-env.git
```

### 2. Inicialize os submódulos

```shell
git submodule init
git submodule update --remote
```

### 3. Construa as imagens e os contêiners

```shell
docker-compose up --build
```

### 4. Execute os scripts do banco de dados

```shell
docker exec -it pdisc-api yarn db:create:tables
docker exec -it pdisc-api yarn db:seeds
```

### 5. Teste se a aplicação está executando

```
http://localhost:8080
```

