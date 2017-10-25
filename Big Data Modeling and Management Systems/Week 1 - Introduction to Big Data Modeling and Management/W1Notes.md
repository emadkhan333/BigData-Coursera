# Introduction to Big Data Modeling and Management

## Summary of Introduction to Big Data

**Three Major Sources of Data**
- Machines
- People
- Organizations

## Ingestion Infrastructure
Ingestion means the process of getting the data into the data system that we are building or using.

**Question to ask for Ingestion Infrastructre**
- How many data sources?
- How large are data items
- Will the number of data sources grow?
- Rate of data ingestion?
- What to do with bad data?
- What to do when data is too little or too much?

## Storage Infrastructure
The goal of a storage infrastructure, obviously, is to store data.
**Question to ask for Ingestion Infrastructre**
- How much data to store?<br /> 
Directly or networkly attached
- How fast do we need to read/write?<br />
Use a memory Hierarchy. SSDs are faster

## Data Quality
Are there ways of knowing if the data is potentially error free and useful for the intended purpose? This is the issue of data quality.
- Poor quality data leads to poor analysis and hence to poor decisions.
- Errors in data in these industries can regulate regulations leading to legal complications. 
- Important for the data to give good quality to gain trust as a leader provider. 

## Data Operations
In general, there are two broad divisions of operations.
- Operations on single data items that produce sub-item.<br/>
For example, an operation that crops an image, that means extracts a sub area from an area of pixels, is a single object operation because we consider the image as a single object. 
- Operations on collections of data objects.<br/>

**Efficiency of Data Operations:**
- Measured by time and space
- Should use parallelism
