# 12 Weeks of AWS

## Building an Event Registration App from POC to Production

A practical 3-month AWS learning and LinkedIn challenge for a recent graduate. The goal is to learn commonly used AWS services by gradually improving one Event Registration application from a simple proof of concept into a secure, scalable, monitored, production-style application.

---

## Challenge Overview

- **Duration:** 12 weeks
- **Publishing schedule:** 2 LinkedIn posts per week
- **Total posts:** 24
- **Primary focus:** AWS services commonly used by Cloud and DevOps teams
- **Application:** Event Registration System
- **Source control:** Git and GitHub
- **Future version:** DevOps tools, Infrastructure as Code, containers and CI/CD

---

## Event Registration Application

The application can include:

- A simple event registration user interface
- A backend API
- A database for registrations
- Event banner or attachment upload
- An admin view for reviewing registrations
- Email notifications

---

# 24-Post Learning Roadmap

## Phase 1: Build the POC Foundation

### Week 1: Application and Source Control

#### Post 1: Starting My 12-Week AWS Challenge: Building an Event Registration App from POC to Production

Introduce the challenge, application idea, planned architecture and learning objectives.

#### Post 2: Managing My Event Registration Application with Git and GitHub

Create the repository, organize frontend and backend folders, add a README, configure `.gitignore`, create branches and practice basic version control.

---

### Week 2: First Deployment

#### Post 3: Launching My First Amazon EC2 Instance for the Event Registration Application

Create an EC2 instance, configure a security group, connect through SSH and understand key pairs.

#### Post 4: Deploying the Event Registration Application on Amazon EC2

Install the application runtime, clone the GitHub repository, configure the application and access it using the EC2 public IP address.

---

## Phase 2: Add Storage and Database

### Week 3: Object Storage

#### Post 5: Storing Event Images and Application Files in Amazon S3

Create a private S3 bucket and use it for event banners, documents or exported registration files.

#### Post 6: Hosting the Event Registration Frontend Using Amazon S3 Static Website Hosting

Separate the frontend from the backend and understand static website hosting. Explain that production access will later move through CloudFront and HTTPS.

---

### Week 4: Database Integration

#### Post 7: Creating an Amazon RDS Database for Event Registrations

Launch a MySQL or PostgreSQL RDS database and understand database configuration, connectivity and security.

#### Post 8: Connecting the EC2 Backend to Amazon RDS

Update the backend to insert, retrieve and display registration records from the database.

---

## Phase 3: Build Secure AWS Networking

### Week 5: VPC Fundamentals

#### Post 9: Building a Custom Amazon VPC for the Event Registration Application

Create a VPC, public and private subnets, route tables and an internet gateway.

#### Post 10: Moving the Application to a Production-Style Public and Private Subnet Architecture

Place the load balancer in public subnets and keep application servers and the database protected in private subnets.

---

### Week 6: Access and Security

#### Post 11: Applying Least-Privilege Access with AWS IAM Roles and Policies

Create an EC2 IAM role for controlled access to S3 and other AWS services instead of storing access keys inside the application.

#### Post 12: Protecting Database Credentials with AWS Secrets Manager

Move database credentials out of configuration files and retrieve them securely from AWS Secrets Manager.

---

## Phase 4: Make the Application Highly Available

### Week 7: Load Balancing

#### Post 13: Adding an Application Load Balancer to the Event Registration App

Create a target group, configure health checks and route incoming requests through an Application Load Balancer.

#### Post 14: Running the Event Registration App Across Multiple Availability Zones

Deploy multiple EC2 instances and test how the load balancer directs traffic to healthy targets.

---

### Week 8: Auto Scaling

#### Post 15: Creating an EC2 Launch Template for Consistent Application Deployment

Create a reusable launch template containing an AMI, instance type, IAM role, security group and user-data bootstrap script.

#### Post 16: Scaling the Event Registration App Automatically with EC2 Auto Scaling

Create an Auto Scaling group, connect it to the load balancer and configure scaling based on demand.

---

## Phase 5: Add Domain, HTTPS and Faster Delivery

### Week 9: DNS and TLS

#### Post 17: Connecting a Custom Domain to the Application with Amazon Route 53

Create a hosted zone and point a Route 53 alias record to the Application Load Balancer.

#### Post 18: Enabling HTTPS with AWS Certificate Manager and an Application Load Balancer

Request a certificate, validate the domain, add an HTTPS listener and redirect HTTP traffic to HTTPS.

---

### Week 10: Content Delivery and Protection

#### Post 19: Speeding Up the Event Registration Website with Amazon CloudFront

Configure CloudFront in front of the application or S3 frontend and understand origins, caching and invalidation.

#### Post 20: Protecting the Public Application with AWS WAF

Create simple managed protection rules, review blocked requests and understand how AWS WAF protects public endpoints.

---

## Phase 6: Operations, Automation and Production Readiness

### Week 11: Monitoring and Notifications

#### Post 21: Monitoring EC2, Load Balancer and Application Health with Amazon CloudWatch

Create dashboards and alarms for CPU utilization, instance health, Application Load Balancer errors, latency and request count.

#### Post 22: Sending Application and Infrastructure Alerts with Amazon SNS

Create an SNS topic and receive email notifications when a CloudWatch alarm changes state.

---

### Week 12: Serverless Automation and Final Architecture

#### Post 23: Automating Event Registration Tasks with AWS Lambda

Create a Lambda function for a supporting task such as generating a registration summary, processing an S3 upload or sending a notification. Lambda supports the application without replacing the complete EC2-based deployment.

#### Post 24: From POC to Production: My Complete AWS Event Registration Architecture

Present the final architecture, AWS services used, security decisions, availability improvements, monitoring setup, GitHub repository and key lessons from the 12-week challenge.

---

# Application Evolution

```text
Local application
    ↓
Git and GitHub
    ↓
EC2 deployment
    ↓
S3 object storage
    ↓
RDS database
    ↓
Custom VPC
    ↓
IAM and Secrets Manager
    ↓
Application Load Balancer
    ↓
Multiple Availability Zones
    ↓
EC2 Auto Scaling
    ↓
Route 53 and HTTPS
    ↓
CloudFront and AWS WAF
    ↓
CloudWatch and SNS
    ↓
Lambda automation
    ↓
Production-style architecture
```

---

# AWS and Supporting Services Covered

## Source Control

- Git
- GitHub

## Compute and Storage

- Amazon EC2
- Amazon EBS
- Amazon S3

## Database

- Amazon RDS
- MySQL or PostgreSQL

## Networking

- Amazon VPC
- Public and private subnets
- Route tables
- Internet gateway
- Security groups
- Application Load Balancer
- Target groups
- Health checks
- Amazon Route 53

## Security

- AWS IAM
- IAM roles and policies
- AWS Secrets Manager
- AWS Certificate Manager
- AWS WAF

## Scalability and Availability

- Multiple Availability Zones
- EC2 Launch Templates
- EC2 Auto Scaling
- Amazon CloudFront

## Monitoring and Automation

- Amazon CloudWatch
- Amazon SNS
- AWS Lambda

---

# Challenge Rules

1. Use **one application throughout all 24 posts** instead of creating unrelated demos.
2. Each post should add one visible improvement to the architecture.
3. Include an architecture diagram, flow diagram or meaningful screenshot in every post.
4. Never commit AWS credentials, private keys, database passwords, secrets or `.env` files to GitHub.
5. Maintain a clear README with architecture, prerequisites, setup instructions, screenshots and cleanup steps.
6. Add a cleanup section to every task to avoid unnecessary AWS costs.
7. Use a consistent naming convention such as `event-app-dev-*`.
8. Add useful tags such as `Project`, `Environment`, `Owner` and `ManagedBy` to AWS resources.
9. Use the AWS Free Tier where applicable, but verify pricing before creating resources.
10. Keep the first version manually deployed so the learner understands each AWS service.
11. Add Infrastructure as Code, containers and CI/CD in Version 2 of the challenge.
12. Remove or mask account IDs, public IPs, domain ownership details and other sensitive information from screenshots before posting publicly.

---

# Suggested GitHub Repository Structure

```text
event-registration-app/
├── frontend/
│   ├── index.html
│   ├── styles/
│   └── scripts/
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── routes/
├── database/
│   └── schema.sql
├── lambda/
│   └── registration-summary/
├── docs/
│   ├── architecture/
│   └── screenshots/
├── scripts/
│   ├── bootstrap.sh
│   └── cleanup.sh
├── .gitignore
├── README.md
└── LICENSE
```

> The exact structure can be adjusted based on the selected frontend and backend technologies.

---

# Recommended Content Format for Each LinkedIn Post

1. **What I built**
2. **Why this AWS service is needed**
3. **How it fits into the Event Registration application**
4. **Main implementation steps**
5. **Challenge or issue faced**
6. **What I learned**
7. **Architecture diagram or screenshots**
8. **GitHub repository link, when applicable**
9. **Question for the audience**

---

# Version 2 Ideas

After completing this AWS-focused challenge, the application can be enhanced with:

- Docker
- Amazon ECR
- Amazon ECS or Amazon EKS
- Terraform or AWS CloudFormation
- GitHub Actions
- CI/CD pipelines
- Automated testing
- Dev, UAT and production environments
- Blue/green or rolling deployments
- Centralized application logging
- AWS Systems Manager
- Cost monitoring and governance

---

## Expected Outcome

At the end of the challenge, the learner should have:

- A working Event Registration application on AWS
- Practical exposure to common AWS services used by DevOps teams
- A GitHub repository showing progressive improvements
- Twenty-four structured LinkedIn learning posts
- A final production-style AWS architecture
- A public portfolio that demonstrates consistent hands-on learning
