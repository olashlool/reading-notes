# Read:08 - LINQ

### Language Integrated Query (LINQ)

Language-Integrated Query (LINQ) is the name for a set of technologies based on the integration of query capabilities directly in the C# language. With LINQ, a query is a first-class language construct, just like classes, methods, events. You write queries against strongly typed collections of objects by using language keywords and familiar operators. By using query syntax, you can perform filtering, ordering, and grouping operations on data sources with a minimum of code. You can use the same basic expression patterns to query and transform data in SQL databases, ADO.NET Datasets, XML documents and streams, and .NET collections.

- Query expressions can be used to query and to transform data from any LINQ-enabled data source. For example, a single query can retrieve data from a SQL database, and produce an XML stream as output.
- Query expressions are easy to master because they use many familiar C# language constructs.

### Introduction to LINQ Queries (C#)

A query is an expression that retrieves data from a data source. Queries are usually expressed in a specialized query language. Different languages have been developed over time for the various types of data sources, for example SQL for relational databases and XQuery for XML. Therefore, developers have had to learn a new query language for each type of data source or data format that they must support. LINQ simplifies this situation by offering a consistent model for working with data across various kinds of data sources and formats. In a LINQ query, you are always working with objects. You use the same basic patterns to query and transform data in XML documents, SQL databases, ADO.NET Datasets, .NET collections, and any other format for which a LINQ provider is available.

#### Three parts of a query operation

1. Obtain the data source
2. Create the query
3. Execute the query

### Basic LINQ Query Operations (C#)

#### Obtaining a Data Source

In a LINQ query, the first step is to specify the data source. In C# as in most prgramming languages a variable must be declared before it can be used. In a LINQ query, the from clause comes first in order to introduce the data source and the range variable.

#### Filtering

Probably the most common query operation is to apply a filter in the form of a Boolean expression. The filter causes the query to return only those elements for which the expression is true. The result is produced by using the where clause. The filter in effect specifies which elements to exclude from the source sequence.

#### Ordering

Often it is convenient to sort the returned data. The orderby clause will cause the elements in the returned sequence to be sorted according to the default comparer for the type being sorted.

#### Grouping

The group clause enables you to group your results based on a key that you specify. When you end a query with a group clause, your results take the form of a list of lists.

#### Joining

Join operations create associations between sequences that are not explicitly modeled in the data sources.

#### Selecting (Projections)

The select clause produces the results of the query and specifies the "shape" or type of each returned element.

