![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/320px-Docker_%28container_engine%29_logo.svg.png)

![](https://grafana.com/static/assets/internal/grafana_logo-web-white-text.svg)
------------------------------
### Comandos utilizados com o docker-compose

 - Parando todos os containers:
 
        docker-compose stop
        
 - Removendo todos os containers:

        docker-compose rm -f
        
 - Verificando o log de todos os containers:

        docker-compose logs -f
        
 - Construir os containers sem inicializá-los:

        docker-compose build
        
 > Os containers criados via `docker-compose` são "comuns", sendo assim os outros comandos do Docker também são válidos. Para maiores detalhes `docker-compose --help`       
