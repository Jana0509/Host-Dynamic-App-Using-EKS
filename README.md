# Host-Dynamic-App-Using-EKS
Host a Dynamic Application with Kubernetes and AWS EKS 

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
    - Designed a **custom VPC** with public, private, and database subnets across multiple Availability Zones.


### **Understanding the EKS Cluster**

- **Control Plane**: Managed by AWS, includes essential components like the API server, scheduler, controller manager, and etcd.
- **Worker Nodes**: Hosts containerized applications. These nodes operate on EC2 instances configured within Auto Scaling groups to handle varying loads efficiently.
- **Networking**: Configured secure communication between the control plane and worker nodes.
- **Monitoring and Logging**: Integrated with **CloudWatch** for real-time monitoring and logging.


### **Key Learning Outcomes**

1. Designed and implemented a **VPC from scratch** with public, private, and DB subnets across multiple Availability Zones.
2. Deployed **Internet Gateway** for internet access to public resources and **NAT Gateway** for private resources to access updates.
3. Built and deployed a **Docker container** for the web app, hosted on **Amazon ECR**.
4. Created and configured **EKS clusters and worker nodes** for high availability.
5. Automated deployment processes with **Kubernetes YAML files** (e.g., `deployment.yaml`, `service.yaml`).
6. Executed database migrations using **Flyway** scripts hosted on **S3**.
7. Utilized **Secrets Manager** to secure credentials for EKS workloads.
8. Deployed **TLS/SSL certificates** to ensure secure communication through **ACM**.
9. Distributed traffic effectively using **NLB** with alias routing via **Route 53**.
