# Public Cloud

## Table of Contents

1. Introduction
2. What is Public Cloud?
3. Why Public Cloud Was Introduced
4. How Public Cloud Works
5. Public Cloud Architecture
6. Characteristics of Public Cloud
7. Components of Public Cloud
8. Real-World Example
9. Production Example
10. Advantages of Public Cloud
11. Disadvantages of Public Cloud
12. When Should You Use a Public Cloud?
13. Public Cloud vs Traditional Infrastructure
14. Popular Public Cloud Providers
15. Key Takeaways

---

# Introduction

Cloud deployment models define **where cloud infrastructure is deployed and who can access it**.

The four major cloud deployment models are:

- Public Cloud
- Private Cloud
- Hybrid Cloud
- Multi-Cloud

Among these, the **Public Cloud** is the most widely used because it provides computing resources over the Internet to anyone who wants to use them.

Companies such as startups, enterprises, educational institutions, and government organizations use public cloud services to reduce costs, increase scalability, and accelerate application deployment.

---

# What is Public Cloud?

A **Public Cloud** is a cloud deployment model where computing resources such as servers, storage, networking, databases, and applications are owned, managed, and maintained by a third-party cloud provider and delivered over the Internet.

The infrastructure is shared among multiple customers (called **multi-tenancy**), but each customer's data and applications remain isolated and secure.

Users pay only for the resources they consume.

### Simple Definition

> **A Public Cloud is a cloud environment where computing resources are owned and managed by a cloud provider and are available to customers over the Internet on a pay-as-you-go basis.**

---

# Why Public Cloud Was Introduced

Before public cloud services, organizations needed to:

- Purchase expensive servers
- Build data centers
- Install networking equipment
- Hire infrastructure engineers
- Maintain hardware
- Upgrade systems regularly

### Problems with Traditional Infrastructure

- High initial investment
- Long deployment time
- Difficult maintenance
- Limited scalability
- Hardware failures
- High operational costs
- Complex disaster recovery

### How Public Cloud Solves These Problems

- No hardware purchase
- Fast deployment
- Automatic scaling
- Global availability
- Pay-as-you-go pricing
- Managed infrastructure
- Built-in backup and disaster recovery options

---

# How Public Cloud Works

A cloud provider owns large data centers around the world.

Customers create resources using:

- Web Portal
- Command Line Interface (CLI)
- APIs
- Infrastructure as Code (Terraform, CloudFormation)

The cloud provider allocates virtual resources from shared physical infrastructure.

Customers can create:

- Virtual Machines
- Databases
- Storage
- Virtual Networks
- Load Balancers
- Kubernetes Clusters

without knowing where the physical servers are located.

---

# Public Cloud Architecture

```text
                   Users
                     │
                 Internet
                     │
              Cloud Provider Portal
                     │
      ┌────────────────────────────────┐
      │      Public Cloud Platform     │
      │                                │
      │  Virtual Machines              │
      │  Storage                       │
      │  Databases                     │
      │  Virtual Networks              │
      │  Load Balancers                │
      │  Kubernetes Clusters           │
      └────────────────────────────────┘
                     │
            Cloud Data Centers
                     │
             Physical Infrastructure
```

---

# Characteristics of Public Cloud

## 1. On-Demand Self-Service

Users can create cloud resources whenever needed without contacting the provider.

Example:

Create a Linux Virtual Machine in five minutes.

---

## 2. Pay-As-You-Go

Customers pay only for the services they use.

Example:

If a virtual machine runs for 10 hours, payment is only for those 10 hours.

---

## 3. Resource Pooling

The cloud provider shares physical resources among multiple customers while keeping their environments isolated.

Example:

Thousands of customers may use the same data center, but each has separate virtual machines and storage.

---

## 4. Rapid Elasticity

Resources can be increased or decreased automatically based on demand.

Example:

An online shopping website automatically adds servers during a festival sale.

---

## 5. Broad Network Access

Cloud services are accessible from anywhere through the Internet.

Example:

Employees working from different countries can access the same application.

---

## 6. High Availability

Applications continue running even if one server fails because workloads are distributed across multiple servers.

---

# Components of Public Cloud

A typical public cloud provides:

- Compute (Virtual Machines, Containers, Serverless)
- Storage (Object, Block, File)
- Networking (VPC, Subnets, VPN, Load Balancers)
- Databases
- Monitoring
- Identity and Access Management (IAM)
- Backup Services
- Disaster Recovery
- Security Services

---

# Real-World Example

Imagine a startup launching an online shopping website.

Instead of purchasing servers, the company creates:

- 2 Virtual Machines
- Managed Database
- Object Storage
- Load Balancer
- Virtual Network

The website becomes available within minutes.

As customer traffic grows, more virtual machines are added automatically.

No hardware purchase is required.

---

# Production Example

An international e-commerce company hosts its application on a public cloud.

```text
                    Users
                      │
                   Internet
                      │
                      DNS
                      │
                     CDN
                      │
               Load Balancer
             ┌────────┴────────┐
             │                 │
       Web Server 1      Web Server 2
             │                 │
             └────────┬────────┘
                      │
            Application Servers
                      │
                Redis Cache
                      │
          Managed Database Cluster
                      │
              Object Storage
                      │
        Monitoring & Backup Services
```

### Workflow

1. Users access the website.
2. DNS resolves the domain name.
3. The CDN serves cached content.
4. The Load Balancer distributes requests.
5. Application servers process business logic.
6. The database stores application data.
7. Object storage stores images and documents.
8. Monitoring continuously checks system health.

---

# Advantages of Public Cloud

## 1. Low Initial Cost

No need to purchase servers or build a data center.

---

## 2. Pay-As-You-Go Pricing

Customers pay only for the resources they actually use.

---

## 3. Easy Scalability

Resources can be increased or decreased within minutes.

Example:

Increase from 2 virtual machines to 20 virtual machines during high traffic.

---

## 4. High Availability

Cloud providers replicate infrastructure across multiple data centers.

Applications remain available even during hardware failures.

---

## 5. Faster Deployment

Infrastructure can be deployed in minutes instead of weeks.

---

## 6. Global Reach

Applications can be deployed in multiple geographic regions.

Example:

A company serves customers in India, Europe, and the United States using different cloud regions.

---

## 7. Automatic Updates

The cloud provider maintains physical servers and infrastructure.

---

## 8. Built-in Security Services

Public cloud platforms provide:

- Firewalls
- Encryption
- Identity and Access Management (IAM)
- Multi-Factor Authentication (MFA)
- Security Monitoring

---

## 9. Disaster Recovery

Cloud providers offer backup and recovery services that reduce downtime after failures.

---

## 10. Supports Modern Technologies

Public cloud platforms support:

- Artificial Intelligence (AI)
- Machine Learning (ML)
- Kubernetes
- Serverless Computing
- Big Data Analytics
- Internet of Things (IoT)

---

# Disadvantages of Public Cloud

## 1. Less Infrastructure Control

Customers cannot control the underlying physical hardware.

---

## 2. Internet Dependency

A stable Internet connection is required to access cloud resources.

---

## 3. Vendor Lock-In

Moving applications from one cloud provider to another can be difficult and expensive.

---

## 4. Security Misconfiguration

Although providers secure the infrastructure, customers must correctly configure their own resources.

Example:

Leaving a storage bucket publicly accessible may expose sensitive data.

---

## 5. Compliance Requirements

Some industries require data to remain in specific countries or private environments.

---

## 6. Variable Monthly Costs

Poor resource management can result in unexpectedly high cloud bills.

---

## 7. Shared Infrastructure

Although customer environments are isolated, the underlying physical infrastructure is shared among many users.

---

# When Should You Use a Public Cloud?

Public Cloud is an excellent choice when:

- You are building a startup application.
- You need to deploy applications quickly.
- You have a limited budget.
- Your workload changes frequently.
- You expect rapid business growth.
- You need global availability.
- You want automatic scaling.
- You are developing or testing applications.
- You are hosting websites or APIs.
- You want managed cloud services instead of maintaining hardware.

### Real-World Use Cases

- E-commerce websites
- Mobile applications
- Online learning platforms
- Streaming services
- Development and testing environments
- Enterprise web applications
- Disaster recovery environments

---

# Public Cloud vs Traditional Infrastructure

| Feature | Traditional Infrastructure | Public Cloud |
|----------|----------------------------|--------------|
| Hardware Purchase | Required | Not Required |
| Initial Investment | High | Low |
| Deployment Time | Weeks or Months | Minutes |
| Scalability | Limited | On Demand |
| Maintenance | Customer | Cloud Provider |
| Global Availability | Limited | Worldwide |
| Payment Model | Capital Expense (CapEx) | Operational Expense (OpEx) |
| Disaster Recovery | Complex | Built-in Services |

---

# Popular Public Cloud Providers

| Cloud Provider | Popular Services |
|----------------|------------------|
| Amazon Web Services (AWS) | EC2, S3, RDS, VPC |
| Microsoft Azure | Virtual Machines, Blob Storage, Azure SQL |
| Google Cloud Platform (GCP) | Compute Engine, Cloud Storage, Cloud SQL |
| Oracle Cloud Infrastructure (OCI) | Compute Instances, Object Storage |
| IBM Cloud | Virtual Servers, Kubernetes Service |

---

# Key Takeaways

- A **Public Cloud** is a cloud deployment model where computing resources are owned and managed by a third-party cloud provider and delivered over the Internet.
- Customers share the provider's physical infrastructure using a secure **multi-tenant** architecture.
- Public cloud offers **high scalability, cost efficiency, global availability, and rapid deployment**.
- It is best suited for **startups, web applications, development and testing environments, APIs, e-commerce platforms, and businesses that require flexible, on-demand infrastructure**.
- Organizations should also consider **Internet dependency, vendor lock-in, compliance requirements, and proper security configuration** when choosing a public cloud solution.