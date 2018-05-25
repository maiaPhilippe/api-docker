# Base-B-api

Api

## Como rodar

``` bash
docker-compose build
docker-compose up -d
```

``` bash
POST http://127.0.0.1:5000/registration {username:name, password:pass}
//Será gerado um token de acesso
```
``` bash
POST http://127.0.0.1:5000/login {username:name, password:pass}
//Será retornado um token de acesso e um token de refresh
```
``` bash
GET http://127.0.0.1:5000/base2?cpf=XXXXXXXXX
Header Bearer TOKEN
// É retornado as informações do CPF
```

### Projeto

ver em diagrama.png

Na relização do projeto acredito que a opção mais segura e estável para os dados seria
o postgres, como opção para utilização de dados para aprendizado de máquina seria utilizado o MongoDb e 
para maior velocidade utilizaria o ElasticSearch.

Neste projeto foi demonstrado o segundo caso (MongoDb) com uma api de autenticação de acesso para todas as
demais Apis, como demonstrado no diagrama.

