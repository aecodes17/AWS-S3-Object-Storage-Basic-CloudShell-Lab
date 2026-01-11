# AWS-S3-Object-Storage-Basic-CloudShell-Lab


 **Overview**
 
This lab demonstrates the basics of Amazon S3 object storage using AWS CloudShell and the AWS CLI.
The goal was to understand how S3 buckets and objects work, how files are created using the command line, and how they are uploaded into S3.

**AWS Services & Tools Used**

Amazon S3
AWS CloudShell
AWS CLI

**What I Learned**

How to create an S3 bucket using the AWS CLI
How object storage differs from traditional file systems
How to create a test file using the echo command
How to upload a file as an object into an S3 bucket
How S3 uses buckets to store objects (not folders)

**Lab Steps**

Step 1: Open AWS CloudShell

AWS CloudShell was launched from the AWS Management Console.
CloudShell provides a browser-based terminal with the AWS CLI already installed and configured.

Step 2: Create an S3 Bucket

A new S3 bucket was created using the AWS CLI.
Bucket names must be globally unique.
aws s3 mb s3://my-first-s3-bucket-12345

Step 3: Verify the Bucket

The bucket was confirmed by listing all S3 buckets.
aws s3 ls

Step 4: Create a Test File Using echo

The echo command was used to quickly create a test file directly in the CloudShell environment.
echo "hello s3" > test.txt


This command:

Outputs the text "hello s3"
Redirects that output into a file named test.txt
Creates the file without opening a text editor

Step 5: Upload the File to the S3 Bucket

The test file was uploaded to the S3 bucket using the AWS CLI.
aws s3 cp test.txt s3://my-first-s3-bucket-12345/test.txt


After upload:

The file became an object in S3
The bucket now contained one object (test.txt)

Step 6: View the Object in the S3 Console

The S3 Management Console was used to visually confirm the object upload.
The file appeared inside the bucket as an object.

**Key Concepts Demonstrated**

Object-based storage
Buckets as containers
Objects as individual files
No real folders in S3
Using CloudShell for AWS CLI commands
Why echo Was Used

The echo command provides a fast way to create test files directly from the command line.
This is useful in cloud environments for testing uploads and understanding storage behavior without needing additional tools.

Summary

This lab provided hands-on experience with Amazon S3 by creating a bucket, generating a test file using echo, and uploading that file as an object using the AWS CLI. It reinforced core S3 concepts such as buckets, objects, and object-based storage.
