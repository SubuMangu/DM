# DM Notes
- **Knowledge Discovery in Databases (KDD)** is a process of extracting useful, non-trivial, and potentially actionable information or patterns from large datasets, often referred to as **data mining**
- The knowledge discovery process is shown in Figure 1.4 as an iterative sequence of the following steps:
    1. **Data cleaning** (to remove noise and inconsistent data)
    2. **Data integration** (where multiple data sources may be combined) 
    3. **Data selection** (where data relevant to the analysis task are retrieved from the
    database)
    4. **Data transformation** (where data are transformed and consolidated into forms
    appropriate for mining by performing summary or aggregation operations)
    5. **Data mining** (an essential process where intelligent methods are applied to extract
    data patterns)
    6. **Pattern evaluation** (to identify the truly interesting patterns representing knowledge
    based on interestingness measures—see Section 1.4.6)
    7. **Knowledge presentation** (where visualization and knowledge representation techniques are used to present mined knowledge to users)

## Tasks involved in data mining
1. **Anomaly Detection**(identification of unusal data records.Eg,outlier analysis)
2. **Association Rule Learning**(relationships between variables)
3. **Clustering** 
4. **Classification**
5. **Regression**
6. **Summarization**(compact representation of Dataset)

## Database System vs Data Warehouse
|Database|Data Warehouse|
|-|-|
|A database system, also called a **database management system (DBMS)**, consists of a collection of interrelated data, known as a database, and a set of software programs to manage and access the data.|A **data warehouse** is a repository of information collected from multiple sources, stored under a unified schema, and usually residing at a single site.|
|A **relational database** is a collection of tables, each of which is assigned a unique name. Each table consists of a set of attributes (columns or fields) and usually stores a large set of **tuples** (records or rows).|A data warehouse is usually modeled by a multidimensional data structure, called a **data cube**, in which each dimension corresponds to an attribute or a set of attributes in the schema, and each cell stores the value of some aggregate measure such as count|
|We use simple query operations written in SQL|We use OLAP operations like drill down and roll up.|
|When mining relational databases, we can go further by searching for trends or data patterns|**Multidimensional data mining** (also called **exploratory multidimensional data mining**) performs data mining in multidimensional space in an OLAP style.That is, it allows the exploration of multiple combinations of dimensions at varying levels of granularity in data mining, and thus has greater potential for discovering interesting patterns representing knowledge.|

## Support and Confidence
- **Support** refers to the probality of a set of items occuring together.

$$support(X, Y)=P(X\cup Y)$$

- **Confidence** is a measure that indicates how likely it is that item Y will appear in a transaction given that item X is already in the transaction. It is a way of evaluating the strength of association between two items.

$$confidence(X \implies Y)=P(Y|X)=\frac{support(X \cup Y)}{support(X)}$$



