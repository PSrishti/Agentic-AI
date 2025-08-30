########################### AWS Regions, Availability Zones, and Edge Locations #########################
An AWS Region is a completely separate geographical area that hosts AWS data centers, these data centers are going to have all of the networking gear, power, servers,etc., that run all of your favorite services in the cloud.
Within Regions, you have Availability Zones, and you're going to see it abbreviated very commonly as AZ, these are isolated, independent locations within a specific region with their own redundant power, networking, and low latency connectivity between one another. AZs are made up of several data centers in a specific area, and each AZ is going to be physically separated to reduce the impacts of disasters. Each region contains at least 3 or more AZs.
The next thing is an Edge Location, these are data centers and other telecommunication providers that have their own data centers to help you deliver services with extremely low latency. These are going to allow you to deploy much closer to your end users compared to using Regions and the AZs within them, they leverage what are called Points of Presence in Regional edge caches.
########################### Responsibility in AWS: The Shared Responsibility Model #######################
<img width="710" height="376" alt="image" src="https://github.com/user-attachments/assets/cd14b44e-8723-4738-8ce2-179e8a857a64" />
################################## AWS well-architected Framework ########################################
Set of principles you should aim to apply to all AWS based workloads : -
Operational Excellence - The ability to >Support development >Run workloads effectively >Gain insights into operations >Continuously improving supporting processes and procedures to deliver business value. Eg. Operations as code, small and frequent changes, using managed services.
Security - Taking advantage of cloud technologies to protect Data, Systems and Assets. Ef. maintaininhg traceability, applying security in layers, encrypting data in transit and at rest, keeping people away from data.
Cost Optimization - The ability to >Run systems that deliver business value  >Operate at the lowest price point. Eg. Adopting a consumption model, measuring overall efficiency, letting AWS handle heavy lifting of infrastructure.
Reliabity - The ability for the workload to  >Peform correctly and consistently. >Be easily tested. Eg. Automating recoveries from failure, testing recovery procedures, scaling horizontally.
Performance Efficiency - Remove bottlenecks, reduce waste. Ability to >Use correct computing resources. >Maintain efficiency with scaling demands. Eg. Using serverless architectures, deploying globally using AWS Regions, experimenting often.
Sustainability - Minimize environmental impacts from workloads. The ability to continually improve sustainability impacts by >Reducing energy consumption  >Increasing efficiency across all components of a workload  >Maximizing the benefits from the provisioned resources  >Minimizing the total resources required. Eg. Understand your impact, maximize utilization, using managed services.


############################################# Core Services ##########################################
AWS IAM - Identity and Access Management
This service provides a unique authentication database that is logically isolated to one AWS account. It provides service to >Create users and grant permissions to those users  >Create groups and roles  >Control access to AWS resources and services. TL;DR - It allowsus to manage users and control their level of access to your AWS account.
For root user accounts (email address used to sign up for AWS), Immediately turn on MFA, Avoid using it for normal tasks, Do not create access keys.

IAM Users and Groups
IAM Users - Entity within IAM meant to represent a human or a dedicated service account
IAM Groups - A collection of IAM users to simplify permission management. Users can belong to multiple IAM groups at a time. No nesting groups.
Long-term credentials - IAM users authenticate via Username and password, or by using static IAM access keys.

