# Desafio 1: Docker para Conversão de Distâncias

Este repositório contém a solução para o Desafio 1 do Desafio DEvOps & Cloud, que visa criar um ambiente Docker para uma aplicação demo de conversão de métricas de distância.

## Informações do desafio

O desafio é parte de um processo de modernização de aplicações da empresa "FakeShop", que busca adotar contêineres para padronizar o ambiente e melhorar a escalabilidade. A aplicação em questão é responsável por converter métricas de distância, como metros para quilômetros e milhas para metros, e foi desenvolvida em Python.

## Cenário

A tarefa prática envolve a configuração do ambiente, a criação e teste do contêiner, e a entrega da solução. O objetivo é criar um Dockerfile que atenda aos requisitos do projeto, gerar uma imagem Docker, executar o contêiner e realizar testes básicos para verificar a funcionalidade de conversão de métricas.

## Tarefa Prática

A solução inclui:

1. Configuração do Ambiente: O Dockerfile criado atende aos requisitos do projeto, instalando as dependências necessárias para a aplicação em Python.
2. Criação e Teste do Contêiner: A imagem Docker é gerada a partir do Dockerfile e o contêiner é executado para garantir que a aplicação esteja acessível na porta 5000. Testes básicos são realizados para verificar a funcionalidade de conversão de métricas.
3. Entrega: A solução é subida em um repositório público, e a imagem do contêiner é publicada no Dockerhub. O link da imagem publicada é incluído neste arquivo README.md.

## Imagem Docker Publicada

A imagem Docker publicada pode ser encontrada no Dockerhub em [seu link aqui](https://hub.docker.com/r/patriciabcatandi/conversao-distancia).

## Instrução para rodar o Docker

Construção da imagem:

```bash
docker build -t patriciabcatandi/conversao-distancia:v1 .
docker build -t patriciabcatandi/conversao-distancia:v1 -f Dockerfile .
```

Cria container

```bash
docker container run -d -p 8181:5000 conversao-distancia
```

Verificar containers

```bash
docker container ls
```bash


Verificar imagens

```bash
docker image ls
```

Criar uma tag a partir de outra

```bash
docker tag patriciabcatandi/conversao-distancia:v1 patriciabcatandi/conversao-distancia:latest
```

Fazer o push para o DockerHub

```bash
docker push patriciabcatandi/conversao-distancia:latest
```