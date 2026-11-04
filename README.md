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


- ### 3. Retrieved an Object from Amazon S3
- The previously uploaded text file was downloaded from the S3 bucket to verify that stored objects could be successfully retrieved.
- The downloaded file was opened locally and its contents were verified, confirming the basic Amazon S3 object storage workflow:
- **Upload → Store → Retrieve**

- ![S3 Object Retrieval](screenshots/03-object-retrieval.png)

- ### 4. Reviewed S3 Block Public Access
- I reviewed the S3 bucket's public access settings and confirmed that **Block all public access** was enabled.
- All four individual Block Public Access settings were enabled to help prevent unintended public access through access control lists (ACLs) and bucket policies.
- The bucket was kept private because this project did not require anonymous or public access to its objects.
- **Key learning** Cloud storage should remain private by default, and access should only be granted when there is a legitimate requirement.
- ![S3 Block Public Access](screenshots/04-block-public-access.png)

- ### 5. Reviewed S3 Bucket Ownership and ACLs
- I reviewed the S3 bucket's Object Ownership setting and confirmed that **Bucket owner enforced** was enabled.
- With this configuration, access control lists (ACLs) are disabled, and the bucket-owning AWS account owns the objects stored in the bucket.
- Access to the bucket and its objects is managed through policies, such as IAM policies and S3 bucket policies, rather than ACLs.
- **Key learning** Using Bucket owner enforced, simplifies ownership and helps centralize access management through policies.
- ![S3 Object Ownership](screenshots/05-object-ownership.png)

- ### 6. Reviewed S3 Bucket Policy
- I reviewed the S3 bucket's resource-based policy configuration and confirmed that no custom bucket policy was attached.
- The AWS Management Console displayed **No policy to display**, while confirming that public access was blocked.
- The project did not require a custom bucket policy because no additional users, applications, or public identities needed access to the stored objects.
- Authorized access to the bucket can be managed through AWS Identity and Access Management (IAM) policies without creating a public bucket policy.
- **Key learning** A bucket does not need a custom bucket policy to function. Permissions should be granted only when there is a specific access requirement.
- ![S3 Bucket Policy](screenshots/06-bucket-policy.png)

- ### 7. Reviewed S3 Default Encryption
- I reviewed the S3 bucket's default encryption setting and confirmed that **Server-side encryption with Amazon S3 managed keys (SSE-S3)** was enabled.
- With SSE-S3, Amazon S3 automatically encrypts objects before storing them and decrypts them when authorized users retrieve them.
- The configuration also showed that **S3 Bucket Key** was enabled and **SSE-C (customer-provided encryption keys)** was blocked.
- SSE-S3 was suitable for this project because it provides encryption at rest without requiring me to create or manage encryption keys manually.
- **Key learning** Encryption at rest protects stored data, while access controls determine who is authorized to access the data. Both are important parts of cloud security.
- ![S3 Default Encryption](screenshots/07-default-encryption.png)

- ### 8. Enabled S3 Bucket Versioning
- I enabled S3 Bucket Versioning to protect stored objects against accidental overwrites and deletions.
- Versioning allows Amazon S3 to preserve multiple versions of an object when a new file is uploaded using the same object key (filename).
- Before enabling versioning, I confirmed that the bucket's versioning status was **Disabled**. I then enabled the feature through the AWS Management Console.
- This configuration prepared the bucket for testing how Amazon S3 retains and recovers previous versions of stored objects.
- **Key learning** S3 Versioning helps protect data by preserving earlier object versions. However, each retained version consumes storage and can increase costs.
- ![S3 Bucket Versioning Enabled](screenshots/08-versioning-enabled.png)

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


## Project Status

In Progress
