# SS7 Anomaly Detection
Anomaly detection for the SS7 Attack Simulator using the ELK stack, Apache
Kafka, and Apache Spark.

This project merges together each component required to run the SS7 Attack
Simulator and analysis its generated traffic using Apache Spark.

## Instructions
Please see the individual subprojects for how to run each individual project.

1. Make sure Elasticsearch and Apache Kafka is running on localhost.
2. Create the Kafka topics *ss7-raw-input* and *ss7-preprocessed*, 
3. Start logstash, which reads network traffic on localhost using tshark: ```logstash -t logstash/tshark-kafka-es.conf```
4. Start the SS7 Attack Simulator following the instructions on the project
   page.
5. Start the ss7-ml-preprocess and the ss7-ml-analysis Spark applications
   following the instructions on the project pages.
6. After some time, data should start to appear in Elasticsearch.
