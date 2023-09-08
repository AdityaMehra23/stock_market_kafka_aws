## Description
The project involves consuming stock market data using Kafka and loading the data into an S3 bucket.
Real-time data streaming is used here. Some examples of real-time sources are Google Maps, Uber, and Amazon (getting notifications of orders purchased, shipped, delivered, etc.). Credit card transactions are also an example of real-time data. We are instantly notified of our transactions. 
Apache Kafka is a distributed event store and stream-processing platform. It is used to build real-time streaming data pipelines and applications that adapt to data streams. 

## Architecture:
<img src="/architecture.png" width="50%" >
Dataset: The data will have information related to the stock market in the form of a CSV file. We are using a static source which is later manipulated to be fed as a stream.
Python program: It will simulate a real-time stock market application. This will use the data to simulate a real-time stock market data stream.
Kafka Producer: This will push the data to Kafka brokers. Kafka is installed on EC2 machine. 
Consumer: It will consume data from the Kafka broker. 
S3: Object storage that will receive data from the consumer and store each record from the stream as a separate file.
Glue crawler: Crawl on the AWS S3 bucket and build tables for the data catalog.
Athena: We can query the data from the AWS Glue Data Catalog and get insights on the stock market data.


**versions**:<br />
Python 3.8.5<br />
Kafka 3.4.0<br />
java 1.8.0_372

