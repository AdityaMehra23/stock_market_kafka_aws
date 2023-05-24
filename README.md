The project involves consuming stock market data using kafka and loads the data into an S3 bucket.
Real time data streaming is used here. Some of examples of real time sources are Google maps, uber, amazon (getting notification of orders purchase, shipped, delivery etc.). Credit card transactions are also an example of real time data. We are instantly notified of our transactions. 
Apache kafka is distributed event store and stream-processing platform. It is used to build real-time streaming data pipelines and applications that adapt to data streams. 

Architecture:
Dataset: The data will have information related to stock market in the form of csv file. We are using a static source which is later manipulated to be fed as a stream.
Python program: It will simulate a real time stock market application. This will use the data from to simulate a real time stock market data stream.
Kafka Producer : This will push the data to kafka brokers. Kafka is installed on EC2 machine. 
Consumer: It will consume data from the kafka broker. 
S3: object storage that will receive data from consumer and store each record from the stream as separate file.
Glue crawler: crawl on the AWS s3 bucket and build tables for data catalog.
Athena: We can query the data from AWS Glue Data Catalog and get insights on the stock market data.

versions:
Python 3.8.5

