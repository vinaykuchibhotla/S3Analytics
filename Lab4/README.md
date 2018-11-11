# S3Analytics

## Introduction
This lab demonstrates the use of Amazon S3 analytics storage class analysis feature for making decisions on data life cycle management policies.

Amazon S3 analytics storage class analysis observes data access patterns and provides recommendations on when to transistion the right data to the right storage class. This new feature determines when to transition less frequently accesses data from STANDARD storage to the STANDARD_IA (IA,for infrequesnt access). For more information about storage classes, see [Storage Classes](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html).

You can use the storage class analysis results for improving the lifecycle policies. You can configure storage class analysis to analyze all the objects in a bucket or you can configure filters to group objects together for analysis by common prefix, by object tags or by both prefix and tags. 


Note: Storage class analysis does not give recommendations for transitions to the ONEZONE_IA or GLACIER storage classes.

You can have multiple storage class analysis filters per bucket, up to 1,000, and will receive a separate analysis for each filter. Multiple filter configurations allow you analyze specific groups of objects to improve your lifecycle policies that transition objects to STANDARD_IA.

Storage class analysis results are updated daily and are available to view from the Amazon S3 console. These results can also be exported to a file in an S3 bucket and can be used in a spreadsheet application or can be used with the business intelligence tools such as Amazon QuickSight.

You can use Amazon S3 Storage Analytics storage class analysis to:
* **Analyze the entire contents of a bucket.**
* **Analyze objects grouped together by prefix and tags.**
* **Export analysis data.**

You can use the Amazon S3 console, the REST API, or the AWS CLI or AWS SDKs to configure storage class analysis. For more information about storage class analysis, see [Amazon S3 Analytics – Storage Class Analysis](https://docs.aws.amazon.com/AmazonS3/latest/dev/analytics-storage-class.html)

## Configuring Storage Class Analysis Lab

1. Go to the S3 console, select your S3 bucket
2. Choose the Management tab, and then choose Analytics.

![Object Properties](../images/SA-choose-management-tab.png)

3. Choose Add

![Object Properties](../images/SA-storage-class-analysis-add-filter.png)

4.Type a name for the filter. If you want to analyze the whole bucket, leave the Prefix / tags field empty.

![Object Properties](../images/SA-storage-class-analysis-filter.png)

5.Name the filter appropriately and in the Prefix/tag filed type text for the prefix or tag for the objects that you want to analyze, or choose from the dropdown list that appears when you start typing.

![Object Properties](../images/SA-storage-class-analysis-prefix.png)




