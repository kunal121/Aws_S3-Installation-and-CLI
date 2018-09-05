# Aws_S3-Installation-and-CLI
## Introduction
Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers.
Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon_uses to run its own global network of web sites. The service aims to maximize benefits of scale and to pass those benefits on to developers.
This guide explains the core concepts of Amazon S3, such as buckets and objects, and how to work with these resources using the Amazon S3 application programming interface (API).

* ### Bucket and Objects
  * An Amazon S3 bucket is a public cloud storage resource available in Amazon Web Services' (AWS) Simple Storage Service (S3), an object     storage offering. Amazon S3 buckets, which are similar to file folders, store objects, which consist of data and its descriptive      metadata.

## Basic Things Need To configure AWS-CLI
    * AWS access ID
    * AWS seceret AccessKey
    * Default Region Name
    * Default Output Format

## IAM(Identify and Access Managment)
Rather than using root user we can allocating rights to each user.So we are using IAM for this and It is a free feature of AWS
* ### Keywords
  * User :- IAM user is anyone who use AWS
  * Group :-Manage a collection of IAM users
  * Role :- Role can be same for multiple user
## AWS-CLI
* ### Installation
    ```
    pip install awscli
    ```
 * ### Verification
    ```
    aws --version
    ```
 * ### Configuration
    ```
    aws --config
    ```
 * ### List all Users,Groups
   ```
   aws iam list-users
   aws iam list-groups
   ```
 * ### Create User,Group,Add_to_group
   ```
   aws iam create-group --group-name
   aws iam add-user-to-group --user_name group --groupname Developers
   ```
 * ### Create new bucket on S3
   ```
   aws s3 mb s3://bucket_name
   ```
 * ### List all Buckets
   ```
   aws s3 ls
   ```
 * ### Upload on s3
   ```
   aws s3 cp 1.txt s3://bucket_name
   ```
 * ### Upload data Recursive(If there is a folder in folder)
   ```
   aws s3 cp . s3://bucket_name --recursive
   ```
 * ### Display all the things present in a bucket
   ```
   aws s3 ls s3://bucket_name
   ```
 * ### Permission while uploading on S3
   ```
   aws s3 cp file_name s3://bucket_name --acl public-read
   ```
 * ### Sync Your Local folder with S3
   We can sync our local folder with the s3 server

   Suppose if there is some data that you recently added to folder but still to be uploaded on s3
   ```
   aws s3 sync .s3//bucket_name
   ```
   Same if you deleted some data from your folder and want to be deleted from s3
   ```
   aws s3 sync .s3//bucket_name --delete
   ```
