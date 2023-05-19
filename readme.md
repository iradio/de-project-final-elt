# Yandex Data Engineer course Final project
This is alternative realisation, based on ELT (not ETL) architecture.

Technical stack:
- docker
- airbyte
- dbt
- postgres
- metabase

Cosist of two repositories:
1. [ELT infrastucture](https://github.com/iradio/de-project-final-elt) 
1. [DBT project](https://github.com/iradio/de-project-final-dbt)

# Start

``` bash
git clone https://github.com/iradio/de-project-final-elt.git
git clone https://github.com/iradio/de-project-final-dbt.git
cd de-project-final-elt
docker-compose up -d
```

# Credentials
Airbyte:`de_user` / `de_pass`

# Worflow

### Extract
Set up Source in Airbyte using [UI](http://localhost:8000).  
![extract](img/extract.png)
### Load 
Set up local Postgres as Destination in Airbyte using [UI](http://localhost:8000).  
![load](img/load.png)
### Transform 
Storing  in separate [repository](https://github.com/iradio/de-project-final-dbt) as DBT prohect . Set up Transofration step in Airbyte using [UI](http://localhost:8000).
![transform](img/transform.png)

