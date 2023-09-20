# E2E Data Engineering Platform
Demo of an example data engineering platform which calls https://randomuser.me/ to generate random names and person information. These data will be streamed via Kafka every 10 seconds using Airflow. The messages will be read by Kafka Consumer using Spark Structured Streaming and will be written to a Cassandra table.
 
stream_to_kafka_dag.py -> Init the Airflow DAG and write the data to a Kafka producer  
stream_to_kafka.py -> Call the API and send data to a Kafka topic 
spark_streaming.py -> Consume the messages of the Kafka topic via Spark Structured Streaming 