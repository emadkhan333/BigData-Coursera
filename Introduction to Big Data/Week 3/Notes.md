# Week 3: Getting Started with Hadoop

## The 4Ws and H of Hadoop

Hadoop Ecosystem is a great for Big Data

1. Enable Scalability
2. Handle Fault Tolerance
3. Optimized for Variety of Data Types
4. Facilitate a Shared Environment
5. Provide Value

**HDFS** is the foundation for many big data frameworks since its provides scalable storage and fault tolerance

**Yarn** provides flexible scheduling and resource management over the HDFS storage

MapReduces is a programming model that simplifies parallel programming.

**Hive** and **Pig** are two additional programming models on top of MapReduce to augment data modeling of MapReduce with relational algebra and data flow modeling respectively.

**Giraph** was built for processing large-scale graphs efficiently

Similarly, **Storm, Spark, and Flink** were built for real time and in memory processing of big data on top of the YARN resource scheduler and HDFS.

NoSQL projects such as **Cassandra, MongoDB, and HBase** handle these cases.

**Zookeeper** is a centralized management system for synchronization, configuration and to ensure high availability.

## The Hadoop Distributed File System

HDFS is comprised of two components. **NameNode** , and **DataNode**. These operate using a master slave relationship. Where the NameNode issues comments to DataNodes across the cluster. The NameNode is responsible for metadata. And DataNodes provide block storage. There is usually one NameNode per cluster, a DataNode however, runs on each node in the cluster.

When the file is created, the NameNode records the name, location in the directory hierarchy and other metadata. The NameNode also decides which data nodes to store the contents of the file and remembers this mapping.

The DataNode runs on each node in the cluster. And is responsible for storing the file blocks. The data node listens to commands from the name node for block creation, deletion, and replication. Replication provides two key capabilities. Fault tolerance and data locality. The default replication factor is three.

## YARN: A Resource Manager for Hadoop

YARN is a resource manage layer that sits just above the storage layer HDFS. YARN enables running multiple applications over HDFC increases resource efficiency and let&#39;s you go beyond the map reduce or even beyond the data parallel programming model.

The **resource manager** controls all the resources, and decides who gets what. Together the resource manager and the node manager form the **data computation framework**. The **container** is an abstract Notions that signifies a resource that is a collection of CPU memory disk network and other resources within the compute note to simplify and be less precise you can think of a container and the Machine.

Benefits of YARN:

- Data -&gt; Extract Value
- One dataset -&gt; Can be run over many applications
- No need to move data around + Higher Resource Utilization -&gt; Lower Cost

## MapReduce

MapReduce is a programming model for the Hadoop ecosystem. It relies on YARN to schedule and execute parallel processing over the distributed file blocks in HDFS. There are several tools that use the MapReduce model to provide a higher level interface to other programming models. Hive has a SQL-like interface that adds capabilities that help with relational data modeling. And Pig is a high level data flow language that adds capabilities that help with process map modeling.

The MapReduce programming model greatly simplifies running code in parallel. Map and reduce are two concepts based on functional programming where the output the function is based solely on the input. For **map** , the operation is applied on each data element. And in **reduce** , the operation summarizes elements in some manner. Map creates a key value pair (key, value).

Next, all the key-values that were output from map are sorted based on their key. And the key values, with the same word, are moved, or shuffled, to the same node.

Next, the reduce operation executes on these nodes to add values for key-value pairs with the same keys.

**Operation of MapReduce:**

1. Map on each node
2. Sort and Shuffle
3. Reduce

**Disadvantages of MapReduces:**

1. Frequent changing data -&gt; mapreduce is slow since it reads input data at each time.
2. Dependent tasks -&gt; maps and reduce work independently
3. Interactive analysis -&gt; mapreduce must read the entire dataset to give results

## Cloud Computing:

The main idea behind cloud computing is to transform computing infrastructure into a commodity. We can simply define a cloud computing service, as a rental service for computing. You rent what you want, and return upon usage.

**Why renting is better than purchasing**

Purchase your own hardware. Then spend on:

- Storage
- Processors
- Networking
- Upgrades

Software Stacks are also complex:

- Latest
- Compatible
- Installation

Other resources required:

- Maintenance
- Procurement
- Disposal
- Quality Control

**Benefits of Clouds:**

- Pay as you go
- Quick Implementation
- Deploy closer to your client
- Resource Estimation solved
- Work on your domain expertise
- Instantly get different resources (CPU, Memory, Disk)

## Cloud Service Models:

IaaS (Infrastructure as a Service) = Get the Hardware Only

- Virtual machines, Servers, Storage, Load Balancers [Amazon EC2]

PaaS (Platform as a Service) = Get the Computing Environment

- Execution runtime, Database, Web server, Development [Microsoft Azure]

SaaS (Software as a Service) = Get full software on-demand

- CRM, Email, Virtual Desktop, Communication, Games [Dropbox]

