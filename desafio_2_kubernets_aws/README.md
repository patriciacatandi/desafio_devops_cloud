# Fake Shop


## Variável de Ambiente
DB_HOST	=> Host do banco de dados PostgreSQL.

DB_USER => Nome do usuário do banco de dados PostgreSQL.

DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.

DB_NAME	=>	Nome do banco de dados PostgreSQL.

DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.

## Fazer o build da imagem e push pro dockerHub

```bash
docker build -t patriciabcatandi/conversao-distancia:v1 . --push
```

Para logar na AWS usando o CLI

```bash
aws configure
```


Para conectar o kubectl com o cluster `aula-eks` criado na AWS
```bash
aws eks update-kubeconfig --name aula-eks
```

Para verificar os nodes

```bash
kubectl get nodes

```


```bash
kubectl apply -f k8s/deployment.yaml
```

Para podermos acessar a aplicação precisamos saber qual domínio ele utilizou
```bash
kubectl get service
```

```bash

```