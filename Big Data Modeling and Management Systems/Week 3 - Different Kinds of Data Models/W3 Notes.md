## Vector Space Model ##
A vector space model is significant for unstructured data. To find text, we not only need the text data itself, but we need a different structure that is computed from the text data. To create the structure, we'll introduce the notion of the document vector model which we call a vector model.
Search engines use some form of vector models and similarity search to locate text data. A _term frequency matrix_ is created with rows against number of words.
After this, we create a new vector called the _inverse document frequency_ for each term. IDF acts like a penalty factor for terms which are too widely used to be considered informative.<br/>
<br/>
Multiplication of the tf numbers with the IDF numbers gives us what we call the **tf-idf matrix**. 
The following are created after that:
- Document Vector
- Query Vector
- Similarity Search

## Graph Data Model ##
Used when data has the form of graphs or networks, the most obvious example being social networks.<br/>
<br/>
What distinguishes a graph from other data models is that it bears two kinds of information? 
  1. Properties and attributes of entities and relationships, 
  2. The connectivity structure that constitutes the network itself.<br/>

A graph is broken down into two tables:
- Vertex Table: or node table, gives IDs to nodes and lists their properties.
- Edge Table:  contains the direction of the arrows in the network and the properties of the edge


