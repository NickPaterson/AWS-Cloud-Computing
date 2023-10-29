# AWS-Cloud-Services PowerPoint

### Contents

1.  [Introduction](#1-introduction)
2.  [What is AWS Cloud Computing](#2-what-is-aws-cloud-computing)
3.  [Types of Cloud Services](#3-types-of-cloud-services)
4.  [Who uses AWS Cloud Services](#4-who-uses-aws-cloud-services)
5.  [AWS Service Categories](#5-aws-service-categories)
6.  [AWS Products](#6-aws-products)
7.  [AWS Lambda](#7-aws-lambda)
8.  [AWS EC2](#8-aws-ec2)
9.  [AWS Storage Gateway](#9-aws-storage-gateway)
10.  [AWS Pros](#10-aws-pros)
11.  [AWS Cons](#11-aws-cons)
12.  [Conclusion](#12-conclusion)
13.  [References](#13-references)


### 1. Introduction

![Slide1](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/99cc2ca9-9607-43db-830b-ef1e539d2480)

A presentation on AWS Cloud Services, presented to the class of COMP10020 - Internet Technologies by: 
Conner Dudfield, Hangning Zhang, Niall Mcgrory, Nick Paterson and Wenxin Xu

![Slide2](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/884bbbcc-85b7-4e8e-9d88-6391dc81e099)
The presentation contents as followed: 
+ What is AWS Cloud Computing
+ Types of Cloud Computing
+ Who Uses AWS Cloud Services
+ AWS Service Categories
+ Products
+ AWS Lambda
+ AWS EC2
+ AWS Storage Gateway
+ Pro and Cons

### 2. What is AWS Cloud Computing
![Slide3](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/fa75dcbe-e64f-4d1f-8d0e-30ed7fc2e1fa)

Cloud computing refers to the delivery of computing services, including servers, storage, networking, databases, analytics, software, and more, over the internet ("the cloud"), (Amazon Web Services, n.d.). ​

Instead of owning and managing physical hardware, users can access and use these resources on-demand from a cloud service provider., such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services (AWS) (Amazon Web Services, n.d.).


### 3. Types of Cloud Services
![Slide4](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/ad93e80b-80e1-4386-ad91-bf4f0ebac2b5)

+ Infrastructure as a Service
+ Platform as a Service
+ Software as a Service 

Each type of cloud computing provides different levels of control, flexibility, and management (Amazon Web Services, n.d.).

![Slide5](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/7d901167-f45b-4b6d-b9fb-0d004658027f)

Infrastructure as a Service (IaaS) is a cloud computing model that provides virtualized computing resources over the internet. ​

In an IaaS model, users can rent virtualized hardware, such as virtual machines, storage, networks, and other infrastructure components from a cloud service provider (Amazon Web Services, n.d.).​


![Slide6](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/4a67fe3a-8e2d-41d2-b521-e4407fc95131)

Platform as a Service (PaaS) is a cloud computing model that provides a platform and environment for developers to build, deploy, and manage applications over the internet. ​

In a PaaS model, the cloud service provider manages and maintains the underlying infrastructure, including servers, storage, and networking, allowing developers to focus solely on writing and deploying code (Amazon Web Services, n.d.).

![Slide7](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/4c7a5d5a-1ace-487a-a178-be06ca0682e5)

Software as a Service (SaaS) is a cloud computing model that delivers software applications over the internet on a subscription basis. ​

In this model, the software is hosted and maintained by a third-party provider, and users can access it via a web browser or a specialized application (Amazon Web Services, n.d.).

### 4. Who uses AWS Cloud Services
![Slide8](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/b68821e6-e97c-4d4b-aa23-db047dec4af7)

AWS is the biggest cloud provider in the world.  Thus, many companies all over the world use AWS. The biggest spenders on AWS (Michalowski, 2023), EC2 monthly spend are: 
1. Sony: $11M 
2. Adobe: $7.5M
3. Facebook: $5.6M
4. Johnson & Johnson: $5M
5. 3M: $5M
6. Coca-Cola: $5M
7. Twitter (X): $3.7M
8. Netflix: $2.4M

### 5. AWS Service Categories 
![Slide9](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/97df7c8d-11f6-41d7-9a40-987ee0c883e7)

The top categories of AWS Services: ​

| Category                 | Description                                                                                     | Key Services                                                 |
| ------------------------ | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Compute Services         | Provide computing resources, allowing you to run applications, host websites, and process data. | Elastic Compute Cloud (EC2), AWS Lambda                      |
| Storage Services         | Offers various storage solutions for your data, ranging from file storage to object storage.    | Amazon E3, Amazon EBS, AWS Storage Gateway                   |
| Database Services        | Offers a wide variety of managed database services including both SQL and NoSQL                 | RDS, DynamoDB, Redshift                                      |
| Networking Services      | Help to establish, manage and secure your network infrastructure.                               | VPC, Direct Connect, Elastic Load Balancing                  |
| Analytics Services       | Designed for processing and analyzing large volumes of data.                                    | EMR, Redshift, AWS Glue                                      |
| AI and Machine Learning  | Offers tools and services for artificial intelligence and machine learning applications.        | Amazon Sage                                                  |
| Content Delivery and CDN | Focused on delivering content and web applications to users with low latency.                   | CloudFront                                                   |
| Developer Tools          | Facilitate application development, deployment, and collaboration.                              | CodeCommit, CodeDeploy, CodeBuild                            |
| Management and Security  | Help to manage, monitor and secure your AWS resources and application.                          | Identity and Access Management (IAM), CloudWatch, CloudTrail |
| Internet of Things (IoT) | Connect and manage IoT devices and process data from them.                                      | IoT Core, IoT Greengrass                                     |

(Amazon Web Services, n.d.) 

### 6. AWS Products
![Slide10](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/22c63f6a-b9db-4d96-bdea-a2f6839f51c3)

As of October 2023, Amazon have a total of 240 products.  A full list is available at [AWS Products](https://aws.amazon.com/products).
In this presentation we will provide an introduction into three of these products:

1. AWS Lambda
2. AWS EC2
3. AWS Storage Gateway

### 7. AWS Lambda
![Slide11](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/eb800952-2a68-4b6a-91f4-148416c964ed)

AWS Lambda is a sеrvicе that allows you to еxеcutе codе without worrying about sеrvеr managеmеnt. ​

It opеratеs basеd on еvеnt triggеrs,  such as filе uploads,  databasе changеs,  or HTTP rеquеsts, which automatically invokе codе.​

AWS Lambda automatically scalеs to handlе workloads,  еnsuring your application is rеsponsivе.  ​

This sеrvеrlеss modеl is cost-еffеctivе,  as you only pay for thе timе your codе runs,  еliminating idlе sеrvеr costs.  It simplifiеs application dеvеlopmеnt by abstracting infrastructurе managеmеnt.  ​

Key features and characteristics of AWS Lambda:

+ Serverless
  + You don't need to worry about server provisioning, scaling, or maintenance. AWS Lambda automatically manages the infrastructure for you.

+ Event-Driven
  + AWS Lambda is designed to respond to events. It can be triggered by various AWS services, custom applications, or HTTP requests using Amazon API Gateway.

+ Supported Runtimes
  +  AWS Lambda supports multiple programming languages, including Node.js, Python, Java, Go, .NET Core, and more. You can use your preferred language to write your functions.

+ Scalability
  +  AWS Lambda scales automatically to handle a high volume of requests. You don't need to configure the scaling behavior.

+ Stateless
  + AWS Lambda functions are stateless, meaning they don't maintain server-specific information between invocations. This makes it easy to run functions in parallel.

+ Integration
  + You can easily integrate AWS Lambda with other AWS services to build serverless applications and microservices.

+ Custom Code
  + You can write custom code to perform specific tasks and execute business logic in response to events. AWS Lambda provides a range of deployment options for your code.

(Amazon Web Services, n.d.).

### 8. AWS EC2
![Slide12](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/fa85fd8a-a7aa-4798-a1e2-1e683c633169)

Amazon Elastic Compute Cloud (Amazon EC2) is one of the core services offered by AWS. It provides resizable compute capacity in the cloud referred to as "instances".

EC2 enables users to run instances on the AWS cloud infrastructure, allowing users to have full control over the virtual server's configuration and scalability.

![Slide13](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/d151876a-b0a2-4bdd-8e4b-54f03242c84b)

+ Scalability ​
  + Allows you to scale computing capacity up or down based on requirements​

+ Various Instance Types​
  + Can be optimised for specific workloads and requirements (CPU, memory, storage and network performance)​

+ Operating System Flexibility ​
  + Supports Amazon Linux, Windows, Ubuntu and more ​

+ Security Groups​
  + Virtual firewalls that control inbound and outbound traffic to EC2 instances​
    
![Slide14](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/86eebdb5-7043-4ee8-b9fe-ae37107fe5ca)

+ Elastic IP Addresses​
  + Elastic IP addresses are static, public IP addresses that you can assign to an EC2 instance​

+ Elastic Block Store (EBS)​
  + Instances can be attached to EBS volumes for storage​

+ Auto Scaling​
  + A feature that automatically adjusts the number of EC2 instances based on define criteria, such as CPU utilisation or network traffic​

+ Load Balancing ​
  + Mechanism to distribute incoming traffic across multiple EC2 instances to ensure high availability, improve fault tolerance and enhance overall performance
  

These features make Amazon EC2 a powerful and flexible service for hosting applications and workloads in the cloud. They enable you to tailor your compute resources to your specific needs, enhance security, and maintain high availability, all while providing the flexibility to grow or shrink your infrastructure as required (Amazon Web Services, n.d.).


![Slide15](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/d96058b9-11a1-4283-8777-22a0881105b9)

| Use Case                   | Description                                                    |
| -------------------------- | -------------------------------------------------------------- |
| Hosting Web Application    | Host web applications and websites.                            |
| Disaster Recovery          | Maintain standby instances for disaster recovery.              |
| Machine Learning           | Train and run machine learning models.                         |
| Game Servers               | Host online multiplayer and gaming servers.                    |
| Databases                  | Host and manage databases for greater control.                 |
| Application Development and Testing | Quickly set up development and testing environments.  |

These are only some of the use cases for an EC2 there are many more things that can be done with an instance. 


### 9. AWS Storage Gateway
![Slide16](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/6ff02ab6-64dc-44bc-ab78-50265094b531)

WS Storage Gateway is a hybrid cloud storage service provided by AWS. It enables you to seamlessly integrate on-premises environments with cloud storage, allowing you to extend your on-premises data center into the AWS Cloud. AWS Storage Gateway offers a range of storage interfaces that can be used to connect your on-premises applications to AWS cloud storage resources (Amazon Web Services, n.d.).

![Slide17](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/015e8694-23fc-4948-94f3-e25f6553661c)

Gateway Types:

+ File Gateway
  + Presents a file-based interface to applications.
  + It supports the Network File System (NFS)
  + Server Message Block (SMB) protocols
  + Enables you to store files in Amazon S3 or Amazon S3 Glacier.

+ Volume Gateway
  + Provides block-based storage and is available in two configurations
    + Cached volumes and stored volumes.
    + Cached volumes store data in Amazon S3 with a cache on-premises

+ Tape Gateway
  + Offers a virtual tape library (VTL) interface to archive data to Amazon S3 and Amazon S3 Glacier.
  + It is used for long-term archival and backup purposes.

### 10. AWS Pros
![Slide18](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/72c32e7d-8655-4251-a177-0108e9be6312)
![Slide19](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/af8496ae-e56b-47cc-a674-c628ac5810da)
![Slide20](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/5720a81a-a3fb-4a61-b16f-04071f364c25)

| Pros                            | Description                                                                                                                                                       |
| ----------------------------    | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Scalability                     | AWS provides on-demand scalability, allowing users to scale resources up or down based on demand. This elasticity is particularly beneficial for applications with varying workloads. |
| Global Reach                    | With data centers located in multiple regions worldwide, AWS allows users to deploy applications globally, reducing latency and improving performance for users across the globe. |
| Comprehensive Service Offering  | AWS offers a vast array of services covering computing, storage, databases, machine learning, analytics, security, IoT, and more. This comprehensive suite enables users to build and deploy diverse types of applications. |
| Cost-Effective                  | AWS follows a pay-as-you-go pricing model, where users only pay for the resources they consume. This can be cost-effective for startups and enterprises alike, eliminating the need for significant upfront investments. |
| Security and Compliance         | AWS implements robust security measures, including encryption, identity and access management, and compliance certifications. This makes it suitable for hosting sensitive data and meeting regulatory requirements. |
| Reliability                     | AWS provides high availability and reliability through redundancy and failover mechanisms. Service Level Agreements (SLAs) guarantee a certain level of uptime for many AWS services. |
| Innovation and Updates          | AWS continually introduces new services and features, staying at the forefront of cloud technology. This allows users to leverage the latest advancements without having to manage infrastructure updates. |
| Community and Support           | AWS has a large and active user community. Additionally, AWS offers extensive documentation, support plans, and a variety of training resources. |


### 11. AWS Cons
![Slide21](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/7f7733e7-a450-4faf-b2b4-7939e534dc70)
![Slide22](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/2dba7126-30fe-45d8-b3c4-2befd7319e9e)
![Slide23](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/79b5341f-0065-4611-8ad9-6a6c867e0143)

| Cons                        | Description                                                                                                                                                       |
| -----------------------------  | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Complexity                    | The richness of AWS services can be overwhelming for beginners, and managing a complex infrastructure may require a learning curve. This complexity can also lead to increased management overhead. |
| Cost Management               | While the pay-as-you-go model is beneficial, it requires careful monitoring to avoid unexpected costs. Complex pricing structures and the multitude of services can make it challenging to estimate expenses accurately. |
| Vendor Lock-In                | Adopting AWS services may create a dependency on the platform, making it challenging to migrate to another cloud provider. Customized configurations and integrations can contribute to vendor lock-in. |
| Downtime and Outages          | Although AWS is designed for high availability, occasional outages can occur. Users should design their applications with redundancy and failover in mind to mitigate potential downtime. |
| Data Transfer Costs           | While data transfer within the same region is often free or inexpensive, costs can escalate for data transfer between regions or over the internet. Users should be mindful of data transfer costs, especially in scenarios with large data volumes. |
| Limited Customization in Serverless Offerings | While AWS Lambda and other serverless offerings provide a convenient and cost-effective way to run code without managing servers, they may have limitations in terms of customization and execution time. |
| Security and Compliance Responsibility | While AWS provides a secure infrastructure, users are responsible for securing their applications and data. Misconfigurations or security lapses on the user's end can lead to vulnerabilities. |
| Support Costs                 | While AWS provides a range of support plans, higher levels of support come with additional costs. Organizations should carefully assess their support needs and associated costs. |


### 12. Conclusion
![Slide24](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/69911331-58ff-4c11-a61c-fb7c42277d02)

In summary, AWS is a powerful and flexible cloud platform, but users need to carefully consider their specific requirements, manage costs effectively, and be prepared for the complexity associated with a comprehensive set of services. The decision to use AWS should align with the organization's goals, technical expertise, and budget considerations.AWS is known for its scalability, flexibility, and cost-effectiveness, making it a popular choice for startups, enterprises, and government organizations looking to leverage cloud computing services. It has data centres in multiple regions globally, providing redundancy and low-latency access to services for users around the world.

![Slide25](https://github.com/NickPaterson/AWS-Cloud-Services/assets/46958743/dff9e6fc-760f-4c29-a147-e8af9f5b79bd)

[EC2 Tutorial](EC2-Tutorial.md)

### 13. References

Amazon Web Services. (n.d.). Amazon EC2. Retrieved from Amazon Web Services: https://aws.amazon.com/ec2/

Amazon Web Services. (n.d.). AWS Cloud Products. Retrieved from AWS: https://aws.amazon.com/products/?aws-products-all.sort-by=item.additionalFields.productNameLowercase&aws-products-all.sort-order=asc&awsf.re%3AInvent=*all&awsf.Free%20Tier%20Type=*all&awsf.tech-category=*all

Amazon Web Services. (n.d.). AWS Lambda. Retrieved from Amazon Web Services: https://aws.amazon.com/lambda/?nc2=h_ql_prod_fs_lbd

Amazon Web Services. (n.d.). AWS Storage Gateway. Retrieved from Amazon Web Services: https://aws.amazon.com/storagegateway/

Amazon Web Services. (n.d.). Types of Cloud Computing. Retrieved from AWS: https://aws.amazon.com/types-of-cloud-computing/?WICC-N=tile&tile=types_of_cloud

Amazon Web Services. (n.d.). What is cloud computing? Retrieved from AWS: https://aws.amazon.com/what-is-cloud-computing/

Michalowski, M. (2023, 07 24). Who’s Using Amazon Web Services? [2023]. Retrieved from Spacelift: https://spacelift.io/blog/who-is-using-aws


