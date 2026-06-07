# Architecture Design

## Overview

This project demonstrates the use of AWS CloudFormation to provision and evolve cloud networking infrastructure using Infrastructure as Code principles.

The architecture was implemented in two stages:

1. Initial Single Availability Zone deployment
2. Updated Multi-Availability Zone deployment

---

## Version 1 - Single Availability Zone

### Architecture

```text
Internet
    │
    ▼
Internet Gateway
    │
    ▼
VPC (10.0.0.0/16)

├── Public Subnet 1 (10.0.0.0/24)
└── Private Subnet 1 (10.0.1.0/24)
```

### Components

* Amazon VPC
* Internet Gateway
* Public Subnet
* Private Subnet
* Public Route Table
* Private Route Table

### Objective

Establish a foundational AWS networking environment using CloudFormation.

---

## Version 2 - Multi Availability Zone

### Architecture

```text
Internet
    │
    ▼
Internet Gateway
    │
    ▼
VPC (10.0.0.0/16)

├── Public Subnet 1 (AZ1)
├── Private Subnet 1 (AZ1)
├── Public Subnet 2 (AZ2)
└── Private Subnet 2 (AZ2)
```

### Enhancements

* Added Public Subnet 2
* Added Private Subnet 2
* Added Route Table Associations
* Extended deployment across two Availability Zones

### Benefits

* Improved Availability
* Improved Scalability
* Better Fault Tolerance
* Foundation for future multi-AZ workloads

---

## Infrastructure Evolution

The architecture was updated through CloudFormation stack updates rather than manual configuration changes.

This approach provides:

* Version-controlled infrastructure
* Repeatable deployments
* Reduced configuration drift
* Improved operational consistency

---

## Deployment Validation

The deployment was validated through:

* CloudFormation Change Sets
* CloudFormation Resource Validation
* CloudFormation Outputs
* Infrastructure Composer Visualization
* Deployment Timeline Review

---

## Key Learning Outcomes

* AWS CloudFormation
* Infrastructure as Code
* Amazon VPC Design
* Multi-AZ Networking
* Stack Updates
* Infrastructure Composer
* Cloud Networking Fundamentals
* Infrastructure Change Management
