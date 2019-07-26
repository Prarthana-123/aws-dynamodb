# Overloading Global Secondary Indexes<a name="bp-gsi-overloading"></a>

Although Amazon DynamoDB has a default limit of 20 global secondary indexes per table, in practice, you can index across far more than 20 data fields\. As opposed to a table in a relational database management system \(RDBMS\), in which the schema is uniform, a table in DynamoDB can hold many different types of data items at one time\. In addition, the same attribute in different items can contain entirely different types of information\.

Consider the following example of a DynamoDB table layout that saves a variety of different kinds of data:

![\[Table schema for GSI Overloading.\]](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/images/OverloadGSIexample.png)

The `Data` attribute, which is common to all the items, has different content depending on its parent item\. If you create a global secondary index for the table that uses the table's sort key as its partition key and the `Data` attribute as its sort key, you can make a variety of different queries using that single global secondary index\. These queries might include the following:
+ Look up an employee by name in the global secondary index, by searching on the `Employee_Name` attribute value\.
+ Use the global secondary index to find all employees working in a particular warehouse by searching on a warehouse ID \(such as `Warehouse_01`\)\.
+ Get a list of recent hires, querying the global secondary index on `HR_confidential` as a partition\-key value and `Data` as the sort key value\.