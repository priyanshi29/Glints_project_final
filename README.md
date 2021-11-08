# Glints_project_final
### Problem Set
A key part of a Data Engineer’s responsibilities is maintaining the serviceability of Data Warehouse. To achieve this, you will need to understand the set up and operation of a basic Data Warehouse.

In this technical assessment, you are required to submit the setup for the data pipeline of a basic data warehouse using Docker and Apache Airflow.

Your final setup should include the following:
- A source postgres database (Database X)
- A target postgres database (Database Y, which is not the same Docker container as Database X)
- Apache Airflow with webserver accessible from localhost:5884
- A Directed Acyclic Graph (DAG) for transferring the content of Source Database X to Target Database Y
- README.md detailing the usage of your submission

As the focus of this technical assessment is on the set up of a basic data pipeline using Airflow, the content of the table in Source Postgres Database X to be transferred can be determined by the candidate. It can be as basic as:

| id | creation_date | sale_value |
| -- | ------------- | ---------- |
| 0  | 12-12-21 | 1000 |
| 1  | 13-12-21 | 2000 |

### Basic Setup 
- Save Dockerfile (without any extension) in the same directory that will be pointing the Docker compose setup
- init.sql and init1.sql these will be used for database commands
- run 'docker build .' command to use the build the image using Dockerfile in the current working directory
- run 'docker-compose up' to setup the required containers, image and data volumes
- /dags/glints_project_data_import.py file has Airflow DAG Python setup script

### PGAdmin Dashboard setup
- Can acccess url http://127.0.0.1:8080/?pgsql=database&username=airflow to verify the data in Source and Target server

### Database Setup
## Source
- Access db using user-name = airflow, password = airflow port = 5833, database = glints_db

## Target
- Access db using user-name = airflow, password = airflow, port = 5834, database = glints_db

