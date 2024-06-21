# DataStreamingETL

Utilizing my background and love for Apache Airflow and data to build a real-time data streaming pipeline, covering each phase from data ingestion to processing and finally storage.

The system is built using Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra — all neatly containerized using Docker for an end to end project! 


## Architecture
![Architecture](/image/DATAETL.png)


- The project is designed with the following components:

    - Data Source: randomuser.me API to generate random user data for the pipeline.
    - Apache Airflow: For orchestrating the pipeline and storing fetched data in a PostgreSQL database.
    - Apache Kafka and Zookeeper: For streaming data from PostgreSQL to the processing engine.
    - Control Center and Schema Registry: For monitoring and schema management of Kafka streams. Control Center listens for events on the Schema Registry to visualize data directly on Kafka that is managed by Zookeeper.
    - Apache Spark: For data processing with master and worker nodes.
    - Cassandra: Where the processed data will be stored.


## Steps to run the project:
1. Clone the repository:

```
git clone https://github.com/prekshivyas/DataStreamingETL.git
```

2. Navigate to the project directory:

```
cd DataStreamingETL
```

Run Docker Compose to spin up the services:

```
docker-compose up
```