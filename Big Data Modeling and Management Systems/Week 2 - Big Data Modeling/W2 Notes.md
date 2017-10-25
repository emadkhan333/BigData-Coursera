# Introduction to Data Model

## What is a Data Model?
Data models describe the data characteristics. The three components of a data model and what they tell us about the data. 
- Structure
- Operations
- Constraints

**Data Model Structures**
There are two type of data model structures
- Structured Data: data that are collection of k fields. (Text, tables)
- Unstructured Data: it's impossible to figure out how the data is organized and how to identify subparts of the data. (Mp3, encrypted data)

**Data Model Operations**
Operations specify the methods to manipulate the data. SInce different data models are typically associated with different structures, the operations on them will be different. But some types of operations are usually performed across all data models. 

Types of Operations:
1. Subsetting: Given a collection of data, and a condition, to perform selection or filtering
2. Substructure Extraction: Given a collection of data, and some structure, extract from each data item a part of the structure as specified by a condition.
3. Union: combinining two data collection to create a new one OR duplicate elimination
4. Join: combining two _different_ data collection to create a new one OR duplicate elimination

**Data Model Constraints**
A constraint is a logical statement. That means one can compute and test whether the statement is true or false. Constraints are part of the data model because they can specify something about the semantics, that is, the meaning of the data. For example, the constraint that a week has seven and only seven days is something that a data system would not know unless this knowledge is passed on to it in the form of a constraint. 

Types of Constraints:
- Value constraint: Age is never negative
- Uniqueness constraint: A movie can only have one title
- Cardinality contraint: a person can between 0 and 3 blood pressure medications at a time
- Type constraint: _Last Name_ is alphabetical
- Domain constraint: possible set of values allowed for that fields; Days can be between 1 and 31

