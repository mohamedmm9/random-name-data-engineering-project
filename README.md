# random-name-data-engineering-project

![image](https://github.com/dogukannulu/kafka_spark_structured_streaming/assets/91257958/2048d405-596c-4921-a938-dcad3d24899e)

Gets random names from the API. Sends the name data to Kafka topics every 10 seconds using Airflow. Every message is read by a Kafka consumer using Spark Structured Streaming and written to the Cassandra table on a regular interval.

`stream_to_kafka_dag.py` -> The DAG script that writes the API data to a Kafka producer every 10 seconds.

`stream_to_kafka.py` -> The script that gets the data from API and sends it to the Kafka topic

`spark_streaming.py` -> The script that consumes the data from the Kafka topic with Spark Structured Streaming


The Random Name Data Engineering project is a comprehensive data pipeline built using Python and various tools such as API, Apache Airflow, Apache Kafka, Apache Spark, Apache Cassandra, and Docker. This project aims to generate and process random name data efficiently and reliably.

The data engineering pipeline begins with an API that generates random names. This API can be developed using Python, allowing users to request a specific number of random names or generate a continuous stream of names. This API acts as a data source for the pipeline.

Apache Airflow is used to orchestrate and schedule the data pipeline. It allows for the creation and management of workflows, defining the tasks to be executed and their dependencies. Airflow ensures that the data pipeline runs smoothly and reliably, enabling data engineers to monitor and troubleshoot any issues that may arise.

Apache Kafka is utilized as a distributed streaming platform to handle the real-time streaming of random name data. Kafka provides a scalable and fault-tolerant messaging system, ensuring the efficient transfer of data between different components of the pipeline.

Apache Spark is employed for data processing and analysis. It is a powerful distributed computing framework that enables high-speed data processing, allowing data engineers to perform complex transformations, aggregations, and analytics on the random names data.

Apache Cassandra is used as a highly scalable and distributed NoSQL database for storing the processed random names data. Cassandra provides a fault-tolerant and highly available storage solution, ensuring data durability and accessibility.

Docker is utilized for containerization, allowing for the easy deployment and management of the various components of the data engineering pipeline. Docker enables the creation of lightweight, isolated containers that encapsulate the dependencies and configurations required for each component, ensuring consistency and portability across different environments.

By leveraging Python and a combination of tools such as API, Apache Airflow, Apache Kafka, Apache Spark, Apache Cassandra, and Docker, the Random Name Data Engineering project provides an efficient and reliable pipeline for generating, processing, and storing random names data. This project can be further extended to include additional data sources, transformations, and analytics, depending on the specific requirements and objectives of the data engineering task.
