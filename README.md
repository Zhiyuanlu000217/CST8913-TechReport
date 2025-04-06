# CST8913-TechReport

Group: 5\
Group Member: Yuntian Du, Xuhui Liang, Zhe Zhang, Zhiyuan, Lu\
Group Section: 011

## Background
Transitioning the company’s infrastructure to AWS is a strategic decision to boost scalability, ensure compliance with regulations like GDPR and HIPAA, and mitigate the risks of outdated systems such as Windows Server 2008 R2 and SQL Server 2008. By refactoring the monolithic ERP system into a modern architecture and rehosting the legacy mainframe on AWS, the company can achieve enhanced performance, reduced downtime, and greater operational flexibility, while meeting critical uptime requirements for business operations.

## ERP system

### migration strategy: Refactor

The ERP system will be refactored by moving from its monolithic structure to a microservices-based architecture on Amazon EKS, upgrading the operating system to Ubuntu 24.04 LTS, migrating the SQL Server 2008 database to Amazon RDS for MySQL, and containerizing the applications for deployment, with CI/CD pipelines implemented via AWS CodePipeline to enhance scalability, maintainability, and resilience.

### architecture diagrams
<img width="389" alt="image" src="https://github.com/user-attachments/assets/d87d9699-7e99-4139-a90b-fa014cb8bb7c" />

### cost estimations
![image](https://github.com/user-attachments/assets/31c27ea6-2cdb-44d6-9b0c-a95024a2b8cd)


## e-commerce applications

### migration strategy: Refactor

The E-commerce applications will be refactored by re-designering its architecture to aligh with modern microservice-based design, that the front-end will hosted on the EKS clusters that runs on top of EC2, both backend and frontend will be containerized, and integrate with CI/CD pipelines. In this case, it will ensure the service's scalability, maintainability, and resilience when company and business grows.

### architecture diagrams

<img width="1039" alt="Screenshot 2025-04-06 at 7 41 26 PM" src="https://github.com/user-attachments/assets/bd65b8f5-8548-4d73-b81b-b979f85e0089" />
Explaination: Consider the scale of the company, the first loadbalancer is used to direct global traffic to differnt EKS cluster, and then, the redirected and distributed traffic will be handled with the kubernetes built in loadbalancer.

### cost estimations
![image](https://github.com/user-attachments/assets/7dba49fe-2900-4454-8e80-4057b3ac7791)

## in-house SQL database cluster and mainframe system

### migration strategy: Rehost(Lift and shift + upgrade)

The legacy mainframe will be rehosted on AWS using AWS Mainframe Modernization tools, migrating its COBOL applications and SQL Server 2008 databases to EC2 instances while retaining Windows Server 2008 R2 and SQL Server 2008 to leverage existing licenses, ensuring a seamless lift-and-shift with AWS Application Migration Service, and maintaining high availability through multi-AZ deployments and robust backup strategies.

### architecture diagrams

There's no architecture changing due to the rehost strategy

### cost estimations

in-house SQL database 
![image](https://github.com/user-attachments/assets/58cd9e5f-a436-4d42-bd79-7fe36644b4f6)

mainframe system
![image](https://github.com/user-attachments/assets/f7612a1b-5df9-4e5c-a42c-7588545b8a4e)



