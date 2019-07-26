# AWS CLI<a name="DAX.create-cluster.cli"></a>

**Topics**
+ [Step 1: Create an IAM service role for DAX to access DynamoDB](DAX.create-cluster.cli.create-service-role.md)
+ [Step 2: Create a Subnet Group](DAX.create-cluster.cli.create-subnet-group.md)
+ [Step 3: Create a DAX Cluster](DAX.create-cluster.cli.create-cluster.md)
+ [Step 4: Configure Security Group Inbound Rules](DAX.create-cluster.cli.configure-inbound-rules.md)

This section describes how to create a DAX cluster using the AWS Command Line Interface \(AWS CLI\)\. If you have not already done so, you will need to install and configure the AWS CLI\. To do this, go to the AWS Command Line Interface User Guide and follow these instructions:
+ [Installing the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)
+ [Configuring the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)

**Important**  
 To manage DAX clusters with the AWS CLI, please install or upgrade to version 1\.11\.110 or higher\. 

**Note**  
All of the AWS CLI examples use the `us-west-2` region and fictitious account IDs\.