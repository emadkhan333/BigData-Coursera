# Data Stream #
Streaming Data Processing Applications is the need to process data as it is generated. An example application would be making data-driven marketing decisions in real time. Through the use of data from real-time sales trends, social media analysis, and sales distributions. Another example for streaming data processing is monitoring of industrial or farming machinery in real time.

## What is a Data Stream ##
A stream is defined as a possibly unbounded sequence of data items or records. That may or may not be related to, or correlated with each other. Each data is generally timestamped and in some cases geo-tagged. As you have seen in our examples, the data can stream from many sources. Including instruments, and many internet of things application areas, computer programs, websites, or social media posts. 
Streaming data sometimes get referred to as event data as each data item is treated as an individual event in a synchronized sequence. 

## Difficulties in Streaming Data ##
Streams pose very difficult challenges for conventional data management architectures. Which are built primarily on the concept of persistence, static data collections. Due to the fact that most often we have only one chance to look at and process streaming data before more gets piled on. Streaming data management systems cannot be separated from real-time processing of data. Managing and processing data in motion is a typical capability of streaming data systems. 

## Dynamic Streaming ##
Dynamic steering is often a part of streaming data management and processing. A self-driving car is a perfect example of a dynamic steering application. But all streaming data applications fall into this category. Amazon Kinesis an other open-source Apache projects like Storm, Flink, Spark Streaming, and Samza are examples of big data streaming systems. Many other companies also provide streaming systems for big data that are frequently updated in response to the rapidly changing nature of these technologies. 


## Data at rest/motion ##
Data-at-rest refers to mostly static data collected from one or more data sources, and the analysis happens after the data is collected. The term data-in-motion refers to a mode although similar data collection methods apply, the data gets analyzed at the same time it is being generated. Just like the sensor data processing in a plane or a self-driving car. Analysis of data addressed is called batch or static processing and the analysis of streaming data is called stream processing. 

The run time and memory usage of most algorithms that process static data, is usually dependent on the data size, and this size can easily be calculated from files or databases. A key property, of streaming data processing is the size of the data is unbounded and this changes the types of algorithms that can be used.  Algorithms that require iterating or looping over the whole data set are not possible since with stream data, you never get to the end. 


# Streaming Data Management and Processing #
The modeling and management of streaming data should enable computations on one data element or a small window of group of recent data elements. These computations can update metrics, monitor and plot statistics on the streaming data. Or apply analysis techniques to the streaming data to learn about the dynamics of the system as a time series. 

Since computations need to be completed in real time, the analysis tasks processing streaming data should be quicker or not much longer than the streaming rate of the data. Which we define by it's velocity. In most streaming systems, the management, and processing system subscribe to the data source, but doesn't send anything back to the stream source in terms of feedback or interactions. These requirements for streaming data processing are quite different than batch processing where the analytical steps have access to often, all data and can take more time to complete a complex analytical task with less pressure on the completion time of individual data management and processing tasks. 

**Lambda Architecture**
Most organizations today use a hybrid architecture. Sometimes get referred to as the lambda architecture for processing streaming and back jobs at the same time. In these systems, streaming wheel over the real-time data is managed and kept until those data elements are pushed to a batch system and become available to access and process as batch data. 

The big data challenges we discussed were scalability, data replication, and durability, and fault tolerance arise in this type of data very significantly. Among many there are two main challenges that needs to be overcome to avoid data loss, and enable real time analytical tasks. One challenge in streaming data process is that the size and frequency of the mean data can significantly change over time. These changes can be unpredictable and may be driven by human behavior. For example, streaming data found on social networks such as Facebook and Twitter can increase in volume during holidays, sports matches, or major news events. 

## Streaming Data vs Static Data ##
Streaming data must be handled differently than static data. Unlike static data, where you can determine the size, streaming data is continually generated, and you can not process it all at once. 
Streaming data can unpredictably change in both size and frequency. This can be due to human behavior. 
Finally, algorithms for processing streaming data must be relatively fast and simple. Since you don't know when the next data arrives.

# Data Lakes #
With big data streaming from different sources in varying formats, models, and speeds it is no surprise that we need to be able to ingest this data into a fast and scalable storage system that is flexible enough to serve many current and future analytical processes. 
This is when traditional data warehouses with strict data models and data formats don't fit the big data challenges for streaming and batch applications. The concept of a data lake was created in response of these data big storage and processing challenges. 

## What is a data lake? ## 
A data lake is a part of a big data infrastructure that many streams can flow into and get stored for processing in their original form. We can think of it as a massive storage depository with huge processing power and ability to handle a very large number of concurrence, data management and analytical tasks. 

"If you think of a datamart as a store of bottled water, cleansed and packaged and structured for easy consumption, the data lake is a large body of water in a more natural state. The contents of the data lake stream in from a source to fill the lake, and various users of the lake can come to examine it, dive in, or take samples. A data lake works as follows." 

The data gets loaded from its source -> stored in its native format until it is needed -> at which time the applications can freely read the data and add structure to it. This is what we call schema on read. In a traditional data warehouse, the data is loaded into the warehouse after transforming it into a well defined and structured format. This is what we call schema on write. Any application using the data needs to know this format in order to retrieve and use the data. 
 
## Data warehouse vs Data Lakes ##
A traditional data warehouse stores data in a hierarchical file system with a well-defined structure. However, a data lake stores data as flat files with a unique identifier. This often gets referred to as object storage in big data systems. 
In data lakes each data is stored as a binary large object or BLOB and is assigned a unique identifier. In addition, each data object is tagged with a number of metadata tags. In Hadoop data architectures, data is loaded into HTFS and processed using the appropriate data management and analytical systems on commodity clusters. 

Summary
- To summarize a data lake is a storage architecture for big data collection and processing. 
- It enables collection of all data suitable for analysis today and potentially in the future. 
- Regardless of the data source, structure, and format it supports storage of data and transforms it only when it is needed. 
- A data lake ideally supports all parts of the user base to benefit from this architecture, including business, storage, analytics and computing experts. 
- Finally, And perhaps most importantly, data lakes are infrastructure components within a big data architecture that can evolve over time based on application-specific needs.  
