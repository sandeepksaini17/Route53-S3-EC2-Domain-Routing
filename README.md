# Domain Routing using Amazon Route 53 with S3 and EC2

## Project Overview

Configured Amazon Route 53 to route:

- www.sandeepaizone.online → Amazon S3 Static Website
- app.sandeepaizone.online → Amazon EC2 Instance

## Services Used

- Amazon Route 53
- Amazon S3
- Amazon EC2
- Elastic IP
- Security Groups

## Architecture

                                  Internet
                                      │
                                      ▼
                          +------------------------+
                          |   Amazon Route 53      |
                          |      Hosted Zone       |
                          +------------------------+
                              │              │
                              │              │
               www.sandeepaizone.online      app.sandeepaizone.online
                              │              │
                              ▼              ▼
                 +------------------+   +------------------+
                 |    Amazon S3     |   |    Amazon EC2    |
                 |  Static Website  |   | Apache / Node.js |
                 +------------------+   +------------------+
                              │              │
                              ▼              ▼
                     Portfolio Website   Dynamic Web App

## Workflow

1. Launch EC2
2. Configure Apache
3. Allocate Elastic IP
4. Create S3 Bucket
5. Enable Static Website Hosting
6. Configure Bucket Policy
7. Configure Route 53
8. Create DNS Records
9. Verify Domain Routing

## Screenshots

## Packet Flow

### 🌐 Flow 1: Static Website (Amazon S3)

```text
User Opens Browser
        │
        ▼
https://www.sandeepaizone.online
        │
        ▼
DNS Request Sent
        │
        ▼
Amazon Route 53
        │
        ▼
Alias Record Lookup
        │
        ▼
Amazon S3 Static Website
        │
        ▼
index.html Returned
        │
        ▼
Website Displayed
```

---

### 🚀 Flow 2: Dynamic Website (Amazon EC2)

```text
User Opens Browser
        │
        ▼
https://app.sandeepaizone.online
        │
        ▼
DNS Request Sent
        │
        ▼
Amazon Route 53
        │
        ▼
A Record Lookup
        │
        ▼
Elastic IP Address
        │
        ▼
Amazon EC2 Instance
        │
        ▼
Apache / Node.js Server
        │
        ▼
Web Page Returned
```

## Learning Outcomes

- DNS Management
- Route 53 Hosted Zones
- Alias Records
- S3 Static Website Hosting
- EC2 Deployment
- Elastic IP Configuration

## Author

Sandeep Kumar# Route53-S3-EC2-Domain-Routing
