# Securely Hosting a Three-Tier Serverless Application on AWS ECS using Terraform

## Overview
This project demonstrates the deployment of a secure, scalable, and serverless web application on Amazon Web Services (AWS) using a three-tier architecture. By leveraging services such as Amazon ECS with Fargate, AWS Lambda, Amazon S3, and MongoDB Atlas, the application framework provides high availability, security, and cost-effective management. Terraform is utilized for Infrastructure as Code (IaC) to automate and ensure consistent deployments across different environments.

## Key Features
- **Three-Tier Architecture**: Divides the application into presentation, logic, and data layers, with strict security measures at each layer.
- **Serverless Deployment**: Uses ECS with Fargate for containerized applications, managed with Terraform to automate infrastructure as code (IaC).
- **Enhanced Security**: Incorporates VPC isolation, IAM role management, encryption (at rest and in transit), and JWT authentication.
- **Scalability and Performance**: Automatically scales according to demand, ensuring optimal performance and cost efficiency.

## Architecture
![Architecture](image.webp)

- **Presentation Layer**: Amazon CloudFront delivers static assets globally for low latency.
- **Logic Layer**: ECS Fargate manages API and backend logic, scaling based on load.
- **Data Layer**: MongoDB Atlas stores application data securely in private subnets with encryption.

## Prerequisites
- **AWS Account**: Ensure permissions for creating VPCs, ECS, Lambda, S3, and other AWS resources.
- **Terraform**: Install Terraform to manage IaC.
- **MongoDB Atlas Account**: For the managed database solution.

## Setup Instructions

1. **Infrastructure Provisioning**: Use Terraform to set up a VPC with public and private subnets across multiple AZs. Security groups, NAT Gateway, and Network ACLs secure resources.

2. **Application Deployment**:
   - **Presentation Layer**: Deploy Amazon CloudFront for static content with HTTPS.
   - **Logic Layer**: Configure ECS Fargate to manage the backend, with automated scaling.
   - **Data Layer**: Connect MongoDB Atlas in private subnets, secured with SSL/TLS.

3. **Security Measures**:
   - **IAM Roles**: Apply the principle of least privilege.
   - **Encryption**: Enable SSL/TLS for data in transit and MongoDB storage encryption.

4. **CI/CD Pipeline**: Automate deployments with GitHub Actions, running Terraform scripts on code changes to ensure consistent environments.

## Testing

- **Security**: Perform penetration testing and IAM policy reviews.
- **Scalability**: Load test ECS Fargate to evaluate scaling capabilities.
- **Performance**: Benchmark latency and response times, optimized by CloudFront and ECS Fargate.

## Screenshot
This screenshot is a part of my project.
![image](https://github.com/user-attachments/assets/57c04715-2207-4327-b3e9-e270d1c32b92)

![image](https://github.com/user-attachments/assets/95329fdd-cd90-43a9-b6cb-c9897f25d328)

![image](https://github.com/user-attachments/assets/a2ca0d61-3ac9-4acf-a111-e3ad23c176ad)

![image](https://github.com/user-attachments/assets/eb1a992a-294b-4d82-9e6f-a892abdfada5)

![image](https://github.com/user-attachments/assets/56ee38ac-5fe3-495f-a665-c7822f98ee34)

![image](https://github.com/user-attachments/assets/c84c4549-0c49-447d-9bbc-6f831e9d1bc1)

![image](https://github.com/user-attachments/assets/bbc13473-8ce2-4fd3-a752-f7a4a31b2b4d)

![image](https://github.com/user-attachments/assets/56a5d1a8-4497-4303-9c76-23d59a451b89)

## Future Improvements
- Multi-region deployment for disaster recovery.
- Enhanced application layer security with AWS WAF.
- Advanced threat detection with AWS GuardDuty.

## References
- [AWS Documentation](https://aws.amazon.com/documentation/)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- [AWS CloudFront Best Practices](https://aws.amazon.com/cloudfront/)
