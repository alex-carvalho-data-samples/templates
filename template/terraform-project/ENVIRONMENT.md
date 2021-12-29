# environment #

## Quick summary  

<img src="img/terraform.png" alt="Terraform" height="30" style="vertical-align: middle;"> Terraform infrastructure containing: 

### network <!--TODO: CHANGE_ME-->

- 1 network called `airflow-celery-net`

### containers <img src="img/docker.png" alt="docker" height="30" style="vertical-align: middle;"> <!--TODO: CHANGE_ME-->

- 1 <img src="img/postgresql.png" alt="PostgreSQL" height="20" style="vertical-align: middle;"> [PostgreSQL](#postgresql)
- 1 <img src="img/airflow.png" alt="Apache Airflow" height="20" style="vertical-align: middle;"> [airflow](#airflow)


# container descriptions #

## PostgreSQL <!--TODO: CHANGE_ME-->

<img src="img/postgresql.png" alt="PostgreSQL" height="60" style="vertical-align: middle;">

### software <!--TODO: CHANGE_ME-->

- PostgreSQL 13.5
- debian 11 (bullseye)

### exposed ports (host:container) <!--TODO: CHANGE_ME-->

- 5432:5432

### container specific info <!--TODO: CHANGE_ME-->

#### database <!--TODO: CHANGE_ME-->
| database name | user    | password |
|---------------|---------|----------|
| airflow_db    | airflow | airflow  |

## airflow <!--TODO: CHANGE_ME-->

<img src="img/airflow.png" alt="Apache Airflow" height="60" style="vertical-align: middle;">

### software <!--TODO: CHANGE_ME-->

- airflow 2.2.2
  - extras
    - celery
    - postgres
    - apache.hive
    - jdbc
    - mysql
    - ssh
    - redis
- python 3.7
- pip 21.2.4
- git 2.20.1
- netcat
- debian 10 (buster)

### exposed ports (host:container)  <!--TODO: CHANGE_ME-->

- 8080:8080

### container specific info  <!--TODO: CHANGE_ME-->

#### URL  <!--TODO: CHANGE_ME-->

http://localhost:8080/

|              |         |
|--------------|---------|
| **Username** | airflow |
| **Password** | airflow |


