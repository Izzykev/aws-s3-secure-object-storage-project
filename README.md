# AWS S3 Static Storage Project

## Project Overview

This project demonstrates the creation and use of an Amazon Simple Storage Service (Amazon S3) bucket using the AWS Management Console.

The objective is to gain hands-on experience with cloud object storage, basic security practices, and technical documentation.

## AWS Service Used

- Amazon S3

## Project Objectives

- Create an Amazon S3 general purpose bucket
- Understand AWS Region selection
- Upload objects to S3
- Retrieve objects from S3
- Review bucket security and permissions
- Document the project using GitHub

## Implementation

### 1. Created an Amazon S3 Bucket

A general purpose S3 bucket was created in the **US East (Ohio) - us-east-2** Region.

The bucket name has been hidden in the public screenshot as a privacy-conscious documentation practice.

![S3 Bucket Created](screenshots/01-s3-bucket-created.png)

### 2. Uploaded an Object to Amazon S3

A sample text file was uploaded to the S3 bucket to verify that the bucket could successfully store objects.

The upload completed successfully, confirming that the bucket was functioning as intended.

![S3 Object Upload](screenshots/02-object-uploaded.png)

## Security Considerations

- AWS access keys and secret access keys are not stored in this repository.
- Sensitive account information is excluded from screenshots.
- The S3 bucket name is hidden where it is not necessary for demonstrating the project.
- Public-access settings will be reviewed carefully before making any object publicly accessible.

## Skills Demonstrated

- Amazon S3
- AWS Management Console
- Cloud storage fundamentals
- Basic AWS security practices
- Git
- GitHub
- Technical documentation

- ### 3. Retrieved an Object from Amazon S3
- The previously uploaded text file was downloaded from the S3 bucket to verify that stored objects could be successfully retrieved.
- The downloaded file was opened locally and its contents were verified, confirming the basic Amazon S3 object storage workflow:
- **Upload → Store → Retrieve**

- ![S3 Object Retrieval](screenshots/03-object-retrieval.png)

## Project Status

In Progress
