# Usando o Heroku + Spring boot

##### * Abrir o terminal a partir do Projeto.

##### * Criar o Repositorio Git:
```
git init
git add .
git commit -am "Start"
git branch -M master
git remote add origin <URL>
git push -u origin master
```
##### * Configurando o Heroku

```
heroku login
heroku create <nome do projeto>
```

Agora é necessario ativar o Postgresql

```
heroku addons:create heroku-postgresql:hobby-dev
```

##### * Fazendo deploy


```
git push heroku master
```

Para acompanhar e verificar os logs do projeto 

```
heroku logs --tail
```

##### * Abrir Aplicação
```
heroku open
```

##### * Usar o Postman para visualizar os dados

Executar a API:

```
(POST) https://nfg-spring-contato.herokuapp.com/contatos

json:
{
    "nome":"Nisflei",
    "email": "ngaloni@gmail.com"
}
```

#### * Shutdown / Start

É necessario executar

```
heroku maintenance:off
heroku maintenance:on
```

###### Referência: https://www.youtube.com/watch?v=dusvP0CFisw
