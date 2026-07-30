# Infrastructure as a Service (IaaS)

## Table of Contents

1. Introduction
2. What is IaaS?
3. Why IaaS Was Introduced
4. How IaaS Works
5. IaaS Architecture
6. Components of IaaS
7. Shared Responsibility Model
8. Real-World Example
9. Production Example
10. Popular IaaS Providers
11. Advantages of IaaS
12. Disadvantages of IaaS
13. IaaS vs Traditional Infrastructure
14. When Should You Use IaaS?
15. Key Takeaways

---

# Introduction

Cloud Computing provides different service models to meet different business requirements. The three major cloud service models are:

- Infrastructure as a Service (IaaS)
- Platform as a Service (PaaS)
- Software as a Service (SaaS)

Among these, **Infrastructure as a Service (IaaS)** is the foundation of cloud computing because it provides the basic infrastructure required to build and run applications.

Instead of purchasing physical servers and building a data center, organizations can rent infrastructure from cloud providers and pay only for what they use.

---

# What is IaaS?

**Infrastructure as a Service (IaaS)** is a cloud computing service model that provides virtualized computing resources such as virtual machines, storage, networking, load balancers, and security services over the Internet.

The cloud provider owns and manages the physical infrastructure, while customers manage the operating system, applications, and data.

### Simple Definition

> **IaaS means renting IT infrastructure from a cloud provider instead of purchasing and maintaining physical hardware.**

---

# Why IaaS Was Introduced

Before cloud computing, companies had to build their own data centers.

A traditional data center required:

- Physical Servers
- Storage Systems
- Networking Devices
- Firewalls
- Cooling Systems
- UPS (Power Backup)
- Internet Connectivity
- IT Administrators

### Problems with Traditional Infrastructure

- High hardware cost
- Long deployment time
- Difficult maintenance
- Limited scalability
- Hardware failures
- Expensive upgrades
- Large IT teams required

### How IaaS Solves These Problems

- No hardware purchase
- Fast deployment
- Pay only for usage
- Easy scaling
- High availability
- Automatic hardware maintenance

---

# How IaaS Works

When a customer requests infrastructure, the cloud provider allocates virtual resources from its data center.

The customer creates:

- Virtual Machines
- Storage
- Virtual Networks
- Firewalls
- Load Balancers

The provider manages the physical infrastructure while the customer manages the software running on it.

### Workflow

```text
Customer Request
        │
        ▼
Cloud Portal / API
        │
        ▼
Create Virtual Machine
        │
        ▼
Attach Storage
        │
        ▼
Configure Network
        │
        ▼
Deploy Operating System
        │
        ▼
Install Applications
```

---

# IaaS Architecture

```text
                     User
                       │
                Cloud Portal/API
                       │
        ┌──────────────┴──────────────┐
        │                             │
 Virtual Machines                 Storage
        │                             │
 Virtual Network              Load Balancer
        │                             │
        └──────────────┬──────────────┘
                       │
                Hypervisor Layer
                       │
              Physical Servers
                       │
                Cloud Data Center
```

---

# Components of IaaS

## 1. Virtual Machines (VMs)

A Virtual Machine is a software-based computer that behaves like a physical server.

Each VM contains:

- CPU
- RAM
- Storage
- Operating System
- Network Interface

### Example

A company launches an Ubuntu virtual machine to host its website instead of purchasing a physical server.

---

## 2. Storage

Storage is used to save operating systems, databases, files, backups, images, and videos.

### Types of Storage

### Block Storage

Used for:

- Virtual Machines
- Databases
- Operating Systems

Example:

Attach a 100 GB SSD disk to a Linux VM.

---

### Object Storage

Stores:

- Images
- Videos
- Documents
- Backups

Example:

An e-commerce website stores product images in cloud object storage.

---

### File Storage

Shared storage that multiple servers can access simultaneously.

Example:

A development team shares project files using cloud file storage.

---

## 3. Networking

Cloud providers offer virtual networking services such as:

- Virtual Private Cloud (VPC)
- Virtual Networks (VNet)
- Subnets
- Public IP
- Private IP
- Route Tables
- Internet Gateway
- NAT Gateway
- VPN

### Example

A company creates:

- Public subnet for web servers
- Private subnet for databases

This improves security because the database is not directly accessible from the Internet.

---

## 4. Load Balancer

A Load Balancer distributes incoming traffic across multiple virtual machines.

### Example

```text
                 Users
                   │
            Load Balancer
             ┌─────┴─────┐
             │           │
          Web VM1     Web VM2
```

### Benefits

- High Availability
- Better Performance
- Automatic Failover
- Scalability

---

## 5. Security

IaaS platforms provide security services such as:

- Firewall
- Security Groups
- Network ACLs
- VPN
- IAM (Identity and Access Management)
- Encryption

### Example

Allow only:

- Port 22 (SSH)
- Port 80 (HTTP)
- Port 443 (HTTPS)

Block all other ports.

---

## 6. Monitoring

Cloud monitoring helps administrators monitor:

- CPU Usage
- Memory Usage
- Disk Usage
- Network Traffic
- Logs
- Application Health

Example tools:

- AWS CloudWatch
- Azure Monitor
- Google Cloud Monitoring

---

# Shared Responsibility Model

The cloud provider and customer share responsibility for managing the infrastructure.

| Component | Cloud Provider | Customer |
|------------|---------------|----------|
| Data Center | ✅ | ❌ |
| Physical Servers | ✅ | ❌ |
| Storage Hardware | ✅ | ❌ |
| Networking Hardware | ✅ | ❌ |
| Hypervisor | ✅ | ❌ |
| Operating System | ❌ | ✅ |
| Applications | ❌ | ✅ |
| Databases | ❌ | ✅ |
| Security Configuration | ❌ | ✅ |
| User Data | ❌ | ✅ |

---

# Real-World Example

### Traditional Method

A startup wants to host an online shopping website.

Without IaaS, it must:

- Buy servers
- Build a data center
- Install operating systems
- Configure networking
- Install web servers
- Purchase backup hardware

This requires a large investment and several weeks of setup.

---

### Using IaaS

The startup logs into AWS, Azure, or Google Cloud and creates:

- 2 Ubuntu Virtual Machines
- 100 GB SSD Storage
- Virtual Network
- Public IP Address
- Firewall Rules
- Load Balancer

The infrastructure is ready within minutes.

---

# Production Example

An e-commerce company expects high traffic during a festival sale.

It deploys the following infrastructure:

```text
                  Internet
                      │
               Load Balancer
             ┌────────┴────────┐
             │                 │
        Web Server VM1    Web Server VM2
             │                 │
             └────────┬────────┘
                      │
             Application Server
                      │
               Database Server
                      │
              Object Storage
```

### Workflow

1. Users access the website.
2. The Load Balancer distributes requests.
3. Web servers process HTTP requests.
4. The Application Server executes business logic.
5. The Database stores customer and order information.
6. Object Storage stores images, videos, and backups.

When traffic increases, additional virtual machines are added automatically.

---

# Popular IaaS Providers

| Cloud Provider | IaaS Services |
|----------------|---------------|
| Amazon Web Services (AWS) | EC2, EBS, VPC |
| Microsoft Azure | Virtual Machines, Virtual Network |
| Google Cloud Platform (GCP) | Compute Engine |
| Oracle Cloud Infrastructure (OCI) | Compute Instances |
| IBM Cloud | Virtual Servers |

---

# Advantages of IaaS

- No need to purchase physical hardware.
- Lower initial investment.
- Pay-as-you-go pricing.
- Rapid deployment.
- Easy scalability.
- High availability.
- Global infrastructure.
- Supports backup and disaster recovery.
- Full control over the operating system.
- Suitable for development, testing, and production workloads.

---

# Disadvantages of IaaS

- Customers must manage the operating system.
- Requires Linux or Windows administration skills.
- Security configuration is the customer's responsibility.
- Costs can increase if resources are left running.
- More management effort compared to PaaS and SaaS.

---

# IaaS vs Traditional Infrastructure

| Feature | Traditional Infrastructure | IaaS |
|----------|----------------------------|------|
| Hardware Purchase | Required | Not Required |
| Initial Cost | High | Low |
| Deployment Time | Weeks or Months | Minutes |
| Scalability | Limited | On-Demand |
| Maintenance | Customer | Provider (Hardware) |
| Payment Model | Capital Expense (CapEx) | Operational Expense (OpEx) |
| Availability | Limited | High |

---

# When Should You Use IaaS?

Use IaaS when you need:

- Full control over the operating system.
- Custom software installation.
- Web hosting.
- Database servers.
- Development and testing environments.
- Disaster recovery.
- Enterprise applications.
- High-performance computing.
- Flexible and scalable infrastructure.

---

# Key Takeaways

- **Infrastructure as a Service (IaaS)** provides virtualized infrastructure such as virtual machines, storage, networking, and security over the Internet.
- The **cloud provider manages the physical infrastructure**, including servers, storage hardware, networking hardware, and virtualization.
- The **customer manages the operating system, applications, databases, and data**.
- IaaS reduces infrastructure costs, enables rapid deployment, and provides scalable resources on demand.
- It is widely used for web hosting, enterprise applications, development environments, disaster recovery, and production workloads.
- Popular IaaS providers include **AWS EC2**, **Azure Virtual Machines**, **Google Compute Engine**, **Oracle Cloud Infrastructure**, and **IBM Cloud**.