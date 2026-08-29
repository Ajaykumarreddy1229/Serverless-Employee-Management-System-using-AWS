# Serverless-Employee-Management-System-using-AWS
**Overview**
This project demonstrates a **serverless web application architecture** deployed on AWS.  
It provides a scalable, secure, and cost‑efficient solution for managing employee data without traditional server management.
Users interact with a static frontend hosted on **Amazon S3**, which communicates with backend services via **Amazon API Gateway** and **AWS Lambda**. Employee records are stored in **Amazon DynamoDB**, ensuring high availability and performance.
**Features**
-->**Serverless Architecture** – No server provisioning or management required  
-->**Highly Scalable** – Automatically scales with demand  
--> **Secure** – SSL/TLS via **AWS Certificate Manager (ACM)** and protection with **AWS WAF**  
-->**Global CDN** – Faster content delivery using **Amazon CloudFront**  
--> **Pay‑as‑you‑go** – Cost‑effective deployment model 

**Technologies Used**
--> **Amazon S3** – Static website hosting (HTML, CSS, JS)  
--> **Amazon CloudFront** – Content Delivery Network (CDN)  
--> **Amazon Route 53** – DNS management with custom domain  
--> **AWS Certificate Manager (ACM)** – SSL/TLS certificates  
--> **AWS WAF** – Web Application Firewall for security  
--> **Amazon API Gateway** – REST API endpoints  
--> **AWS Lambda** – Serverless compute functions  
--> **Amazon DynamoDB** – NoSQL database for employee data  
**API Endpoints**
--> POST /employeeData` → Insert new employee record  
-->GET /employeeData` → Retrieve employee records  
**Database Details**
--> **Table Name:** employeeData
--> **Primary Key:** employeeid (String)
**Project Flow**
1. User accesses application via **Route 53** (custom domain).  
2. Request secured with **ACM SSL/TLS** and filtered by **AWS WAF**.  
3. **CloudFront** delivers static frontend files from **S3**.  
4. Frontend makes HTTPS API calls to **API Gateway**.  
5. **API Gateway** routes requests to **Lambda functions**.  
6. **Lambda** interacts with **DynamoDB** for CRUD operations.  
7. Response returned to the user.  
**Key Benefits**
--> Zero server management  
--> Secure and scalable  
--> Cost‑efficient with pay‑per‑use model  
--> Easy integration with AWS ecosystem
**How to Deploy**
1. Upload frontend files (HTML, CSS, JS) to **Amazon S3** bucket.  
2. Configure **CloudFront** distribution with S3 as origin.  
3. Set up **Route 53** for custom domain routing.  
4. Attach SSL certificate via **ACM**.  
5. Enable **AWS WAF** for security filtering.  
6. Create **API Gateway** endpoints (`POST`, `GET`).  
7. Implement **Lambda functions** for business logic.  
8. Create **DynamoDB table** (`employeeData`) with primary key `employeeid.
**Future Enhancements**
--> Add authentication with **AWS Cognito**  
--> Implement CI/CD pipeline with **AWS CodePipeline**  
--> Add monitoring with **Amazon CloudWatch**  
