The project involves consuming stock market data using kafka and loads the data into an S3 bucket.
Real time data streaming is used here. Some of examples of real time sources are Google maps, uber, amazon (getting notification of orders purchase, shipped, delivery etc.). Credit card transactions are also an example of real time data. We are instantly notified of our transactions. 
Apache kafka is distributed event store and stream-processing platform. It is used to build real-time streaming data pipelines and applications that adapt to data streams. 

Architecture:
Dataset: The data will have information related to stock market in the form of csv file. 
Python program: It will simulate a real time stock market application.
Kafka Producer : will push the data to kafka brokers. Kafka is installed on EC2 machine. 
Consumer: take data from broker
S3: object storage that will receive data from consumer
Glue crawler: crawl schema out of s3 files and build glue data catalog.
Glue data catalog: catalog build from s3 files.
Athena: querying data from glue data catalog.  

