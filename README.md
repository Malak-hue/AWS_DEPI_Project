This document outlines the architecture and components used to build a highly available, scalable web 
application on AWS.  
The project aims to improve the performance of a student records web application during peak admissions 
periods by leveraging AWS services. 
overview of the key AWS components used to build a highly available, scalable, and 
secure web application. Each component plays a crucial role in ensuring the application meets performance 
and security requirements, especially during peak usage periods. The architecture is designed following AWS 
best practices to optimize cost, scalability, and high availability. 
Key Components 

• Virtual Private Cloud (VPC): Establishes a secure network environment with isolated resources, 
including public and private subnets across multiple Availability Zones for redundancy. 

• Amazon EC2 Instances: Hosts web applications, providing compute power with flexibility. 

• Amazon RDS: Manages the relational database independently from the application servers. Configured 
with MySQL engine in a multi-AZ deployment for high availability. 

• AWS Secrets Manager: Secures sensitive information like database credentials, enabling secure access 
by the web application without hardcoding credentials. 

• Application Load Balancer (ALB): Distributes incoming traffic across multiple EC2 instances to ensure 
load balancing and high availability.  

• Auto Scaling Group: Automatically adjusts the number of EC2 instances based on demand to maintain 
performance. 

• AWS Cloud9: Provides a cloud-based development environment for managing and deploying code. 

• AWS WAF (Web Application Firewall): Protects the web application from common web exploits and 
bot traffic by filtering harmful requests before they reach the application. 

• Amazon CloudWatch: Monitors application performance and resource utilization, providing insights 

and alerts to maintain operational health and efficiency. 

• AWS Backup: Centralizes backup management for AWS resources, ensuring data protection and 
compliance through automated scheduling of backups for RDS and EC2 volumes. 
Each component has been carefully selected and configured to ensure that the application remains responsive 
and secure, even under heavy load. The following sections will delve into the purpose and configuration of 
each component in detail.
