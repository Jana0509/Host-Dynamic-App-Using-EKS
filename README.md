# Host-Dynamic-App-Using-EKS
Host a Dynamic Application with Kubernetes and AWS EKS 

### Introduction:
This Project demonstrates deploying the dynamic application in Elastic Kubernetes cluster. A Containerized Application is deployed in EKS Cluster in the private subnets and and its fronted with the Network Load Balancer for routing the traffic across multiple availability zones and storing the data in RDS(Relational Database Service) also sitting in private subnet. To connect the Private instances, EC2 Instance Connect Endpoint Service for secure SSH access. It leverages end-to-end cloud-native deployment process, showcasing AWS best practices for scalability, security, and cost-efficiency. By combining industry-standard tools with AWS services, the architecture is resilient, secure, and scalable for modern dynamic applications.

### Architecture
![image](https://github.com/user-attachments/assets/9b1a00f4-f0c1-41fa-b701-4911ca6686f9)



### **Project Highlights**

1. **Version Control**:
   - Used **Git and GitHub** for seamless code deployment and storing the codebase efficiently.

2. **Containerization**:
   - Containerized the dynamic web application using **Docker** to ensure consistent runtime environments.

3. **RDS MySQL**:
   - Created and configured **RDS MySQL** to serve as the database for the application.

4. **EKS Cluster**:
   - Deployed the containerized web application to an **Elastic Kubernetes Service (EKS) Cluster**, ensuring scalability and resilience.

5. **Kubernetes Tools**:
   - Managed Kubernetes clusters using **kubectl**, **eksctl**, and **Helm** for streamlined operations.

6. **EC2 Instance Connect**:
   - Deployed **EC2 Instance Connect Endpoint** within the private subnet for secure access.

7. **TLS/SSL Encryption**:
   - Generated and stored **TLS/SSL certificates** using **AWS Certificate Manager (ACM)** for in-transit encryption.

8. **Secrets Manager**:
   - Stored cluster credentials securely in **Secrets Manager**, ensuring safe and centralized access.

9. **Database Migration**:
   - Used **S3** to store and execute **Flyway DB scripts** for migrating data to RDS MySQL.

10. **Elastic Container Registry (ECR)**:
    - Set up **ECR** to store Docker images for streamlined deployment to EKS.

11. **Route 53**:
    - Created a **Route 53** alias record to route traffic to the Network Load Balancer (NLB).

12. **IAM**:
    - Configured **IAM roles and policies** for secure access control.

13. **Load Balancer**:
    - Deployed a **Network Load Balancer (NLB)** in public subnets to distribute traffic efficiently across the cluster in multiple AZs.

14. **VPC Setup**:
    - Designed a **custom VPC** from the scratch with public, private, and database subnets across multiple Availability Zones.


### **Understanding the EKS Cluster**

- **Control Plane**: Managed by AWS, includes essential components like the API server, scheduler, controller manager, and etcd.
- **Worker Nodes**: Hosts containerized applications. These nodes operate on EC2 instances configured within Auto Scaling groups to handle varying loads efficiently.
- **Networking**: Configured secure communication between the control plane and worker nodes.
- **Monitoring and Logging**: Integrated with **CloudWatch** for real-time monitoring and logging.


### **Key Learning Outcomes**

1. Designed and implemented a **VPC from scratch** with public, private, and DB subnets across multiple Availability Zones.

![image](https://github.com/user-attachments/assets/113e04c2-9b46-42f1-abbe-209f87538f36)
![image](https://github.com/user-attachments/assets/0deb091a-46e8-4232-9553-37a03618a41a)

2. Deployed **Internet Gateway** for internet access to public resources and **NAT Gateway** for private resources to access updates.
3. Built and deployed a **Docker container** for the web app, hosted on **Amazon ECR**.

![image](https://github.com/user-attachments/assets/75557f19-bea4-4804-8837-d6283e520098)

4. Created and configured **EKS clusters and worker nodes** for high availability.

![image](https://github.com/user-attachments/assets/ac56b3f9-bf25-4b36-9ec4-0834aca0af52)
![image](https://github.com/user-attachments/assets/d0c54171-e976-4bc3-ae90-3156718cb206)

5. Automated deployment processes with **Kubernetes YAML files** (e.g., `deployment.yaml`, `service.yaml`).
6. Executed database migrations using **Flyway** scripts hosted on **S3**.
7. Utilized **Secrets Manager** to secure credentials for EKS workloads.

![image](https://github.com/user-attachments/assets/93d27931-8f04-40bf-9dbb-a1f3256c1156)


8. Deployed **TLS/SSL certificates** to ensure secure communication through **ACM**.
9. Distributed traffic effectively using **NLB** with alias routing via **Route 53**.

![image](https://github.com/user-attachments/assets/55ae24e2-1a3e-403f-ba91-88bdad8d209d)

![image](https://github.com/user-attachments/assets/895310fb-8193-48a8-b099-4720d41fd4f1)
    
### Conclusion:
In conclusion, this project highlights the successful implementation of a dynamic application hosted on an AWS EKS Cluster, following cloud-native principles. By leveraging AWS's robust services and integrating best practices, the architecture delivers high scalability, resilience, and security while remaining cost-efficient. This hands-on experience reinforces the practical knowledge of designing, deploying, and managing cloud-based applications, making it a significant step forward in mastering modern application hosting solutions.
