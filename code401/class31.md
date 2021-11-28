# S3

## What is Amazon S3?

Amazon Simple Storage Service (Amazon S3) is storage for the Internet. Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, and inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites.

## Advantages of using Amazon S3

- Creating buckets – Buckets are the fundamental containers in Amazon S3 for data storage.

- Storing data – Store an infinite amount of data in a bucket. Upload as many objects as you like into an Amazon S3 bucket.

- Downloading data – Download your data or enable others to do so. Download your data anytime you like, or allow others to do the same.

- Permissions – Grant or deny access to others who want to upload or download data into your Amazon S3 bucket.

- Standard interfaces – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.

## Amazon S3 concepts

**[Buckets]**
A bucket is a container for objects stored in Amazon S3. Every object is contained in a bucket. Buckets serve several purposes:

- They organize the Amazon S3 namespace at the highest level.

- They identify the account responsible for storage and data transfer charges.

- They play a role in access control.

- They serve as the unit of aggregation for usage reporting.

**[Objects]**

Objects are the fundamental entities stored in Amazon S3. An object is uniquely identified within a bucket by a key (name) and a version ID.

**[Keys]**

A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key.

**[Regions]**

You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create.

**[Amazon S3 data consistency model]**

Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions.

## Amazon S3 features

- Storage classes
- Bucket policies
- AWS Identity and Access Management
- Access control lists
- Versioning
- Operations

## Amazon S3 application programming interfaces (API)

The Amazon S3 architecture is designed to be programming language-neutral, using AWS Supported interfaces to store and retrieve objects. Amazon S3 provides a REST and a SOAP interface. They are similar, but there are some differences.

> Note: SOAP support over HTTP is deprecated, but it is still available over HTTPS.

## Paying for Amazon S3

Amazon S3 charges you only for what you actually use, with no hidden fees and no overage charges. This gives developers a variable-cost service that can grow with their business while enjoying the cost advantages of the AWS infrastructure.