# Databricks Strimzi Kafka Oauth Shaded Library

Databricks cloud platform internally shaded Kafka library from
org.apache.kafka to kafkashaded.org.apache.kafka. Many Kafka client is 
built on org.apache.kafka. This sample project shows how to quickly shade
Kafka client library to be compatible with Databricks' shaded Kafka library.


The project uses maven shade plugin to relocate Kafka client library from
org.apache.kafka to kafkashaded.org.apache.kafka and builds a fat jar


The project uses Strimzi kafka-oauth-client as example to show how to build
a databricks compatible library

      <groupId>io.strimzi</groupId>
      <artifactId>kafka-oauth-client</artifactId>
      <version>0.3.0</version>

## How to use
* Run maven clean install
* The shaded library is at databricks-strimzi-kafka-oauth/target/databricks-shaded-strimzi-kafka-1.0.jar
