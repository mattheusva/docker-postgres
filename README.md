# PostgreSQL e pgAdmin com Docker

Um script Docker Compose para instalar localmente o PostgreSQL e o pgAdmin de forma rápida.

## Requisitos
 - Docker
 - Docker Compose
## Como executar

Primeiro é necessário criar uma rede para os Containers. Rode o seguinte comando:
```
docker network create local-network
```
Suba os containers utilizando docker compose
```
docker compose up
```

## Utilizando o pgAdmin
Para testar se o serviço do pgAdmin está funcionando acesse http://localhost:8080 no seu navegador, haverá uma tela de autenticação, você deverá informar o email e senha que definimos no docker-compose.yml.

Clique em adicionar novo servidor e de um nome para ele.

![novo servidor](https://github.com/mattheusva/docker-postgres/assets/99608627/7ab0ed30-b04c-44a5-afca-b9ff749e87c7)
<br>

Na aba Conexão e no campo **host name** informe o nome do Container do Postgres e no campo **username** e **senha** colocar os mesmos que foram definidos no Compose.

![Captura pgadmin](https://github.com/mattheusva/docker-postgres/assets/99608627/057d4276-20f5-499b-a3a5-50eacb51c432)

---

**Pronto! agora você tem um ambiente com PostgreSQL e o pgAdmin web.**
