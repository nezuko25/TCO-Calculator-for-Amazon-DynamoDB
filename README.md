# TCO-Calculator-for-Amazon-DynamoDB
To estimate the cost of the DynamoDB table, we can use an [AWS calculator](https://calculator.aws/#/) and [DynamoDB+Cost+Template.xlsx](https://github.com/awslabs/amazon-dynamodb-tools?tab=readme-ov-file#cost-template). You may also want to calculate the costs related to global tables supporting multiple regions and also related to the table class to understand what the best selection is to optimize the table cost.

This worksheet will help you estimate a table's cost of ownership in multiple regions, either regionally or globally. Not just that, this will help you see if Standard Table Class or Standard-IA Class will be a cost-efficient choice.

When it comes to the global table, the cost is with respect to replicated WCUs and storage in other regions. Hence, this is a straight-up cost where no optimizations can be made. Under some scenarios, the replicas are used only for disaster recovery, where they are sitting idle and will only have read traffic when one region goes down. Another scenario is that some replicas have fewer RCUs than other regions. Hence, you can try to see if the Standard IA table class can help if the storage cost of these replicas is the driving cost for these tables.

The unit prices that are considered to do the calculation are as per the current prices in every region. Because prices may change in the future, you can adjust these as needed for a specific region under the specific worksheet (separate for each region).

The tool will help you model the table costs across replicas with Standard and Standard IA table classes. Please refer to the DynamoDB Pricing Page for a full list of DynamoDB features, options, and prices. 

**Note:**
1) This is just an estimation of the cost. Please do not co-relate with the cost incurred towards your account as the comsumption will change as per the usecase.
2) Sheet 1 of the worksheet will help you to fill in the necessary fields to get the costs.




