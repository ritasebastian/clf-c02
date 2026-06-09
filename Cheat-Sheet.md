
# AWS CLF-C02 "Service → Usage" Cheat Sheet

## Storage & Data Transfer

| Service                | Memory Hook            | Use When You See                               |
| ---------------------- | ---------------------- | ---------------------------------------------- |
| Amazon S3              | "Store anything"       | Object storage, backups, static websites, logs |
| S3 Glacier             | "Archive"              | Long-term backup, rarely accessed data         |
| S3 Intelligent-Tiering | "Auto move"            | Unknown access patterns                        |
| EBS                    | "Hard drive for EC2"   | Block storage attached to one EC2              |
| EFS                    | "Shared Linux drive"   | Multiple EC2 instances share files             |
| FSx                    | "Managed file server"  | Windows or specialized file systems            |
| Storage Gateway        | "Bridge to cloud"      | Hybrid storage, tape replacement, local cache  |
| DataSync               | "Fast file mover"      | Transfer files between on-prem and AWS         |
| Snowball Edge          | "Truck-sized transfer" | TB–PB data migration                           |
| Snowmobile             | "Shipping container"   | 10+ PB, huge migrations                        |

### Mnemonic

**Store → S3**
**Share → EFS**
**Attach → EBS**
**Hybrid → Storage Gateway**
**Move → DataSync**
**Massive Move → Snow Family**

---

## Compute

| Service           | Memory Hook           | Use When You See                        |
| ----------------- | --------------------- | --------------------------------------- |
| EC2               | Virtual servers       | Full control                            |
| Lambda            | No servers            | Event-driven, short jobs                |
| Elastic Beanstalk | Upload code           | AWS manages infrastructure              |
| Fargate           | Serverless containers | Run containers without managing servers |
| Auto Scaling      | Automatic EC2 scaling | Scale in/out with demand                |
| AppStream 2.0     | Stream applications   | Powerful app on weak laptops            |
| WorkSpaces        | Cloud desktop         | Remote employees                        |

### Mnemonic

**Server → EC2**
**No Server → Lambda**
**Container No Server → Fargate**
**Desktop → WorkSpaces**
**Application Streaming → AppStream**

---

## Databases

| Service  | Memory Hook           | Use When You See           |
| -------- | --------------------- | -------------------------- |
| RDS      | Managed relational DB | MySQL, PostgreSQL, MariaDB |
| Aurora   | Faster MySQL/Postgres | High performance           |
| DynamoDB | NoSQL serverless      | Auto-scaling key-value DB  |
| Redshift | Data warehouse        | Analytics                  |
| Neptune  | Graph database        | Relationships              |

### Mnemonic

**SQL → RDS**
**Fast SQL → Aurora**
**NoSQL → DynamoDB**
**Analytics → Redshift**

---

## Networking

| Service            | Memory Hook             | Use When You See        |
| ------------------ | ----------------------- | ----------------------- |
| Route 53           | DNS                     | Domain routing          |
| CloudFront         | CDN                     | Global content delivery |
| Direct Connect     | Dedicated link          | Consistent low latency  |
| Site-to-Site VPN   | Quick secure connection | Connect on-prem to AWS  |
| Transit Gateway    | Network hub             | Multiple VPCs           |
| Global Accelerator | Fast global app access  | Cross-region failover   |
| Internet Gateway   | Internet access         | Public subnet           |

### Mnemonic

**DNS → Route 53**
**CDN → CloudFront**
**Dedicated Network → Direct Connect**
**Many VPCs → Transit Gateway**

---

## Security

| Service      | Memory Hook           | Use When You See           |
| ------------ | --------------------- | -------------------------- |
| IAM          | Who can do what       | Users, groups, permissions |
| IAM Role     | Temporary access      | EC2 → AWS services         |
| STS          | Temporary credentials | Short-lived access         |
| GuardDuty    | Threat detection      | Suspicious activity        |
| Inspector    | Vulnerability scanner | EC2 security assessment    |
| Macie        | Sensitive data finder | S3 PII discovery           |
| Security Hub | Security dashboard    | Aggregate findings         |
| Shield       | DDoS protection       | Attack protection          |
| WAF          | Web firewall          | Block IPs/countries        |
| CloudTrail   | Who did what          | Audit logs                 |
| Artifact     | Compliance reports    | SOC, PCI, ISO              |

### Mnemonic

**Who? → IAM**
**Temporary? → Role / STS**
**Threats? → GuardDuty**
**Vulnerabilities? → Inspector**
**Sensitive Data? → Macie**
**Audit? → CloudTrail**

---

## Monitoring & Management

| Service         | Memory Hook            | Use When You See |
| --------------- | ---------------------- | ---------------- |
| CloudWatch      | Metrics & alarms       | Monitoring       |
| CloudTrail      | API activity           | Audit            |
| Config          | Resource configuration | Compliance       |
| Trusted Advisor | Best practices         | Recommendations  |
| EventBridge     | Event routing          | Trigger actions  |

### Mnemonic

**Watch → CloudWatch**
**Track API Calls → CloudTrail**
**Configuration → Config**

---

## Cost Optimization

| Service              | Memory Hook          | Use When You See        |
| -------------------- | -------------------- | ----------------------- |
| Cost Explorer        | Analyze spending     | Historical costs        |
| AWS Budgets          | Alerts               | Budget thresholds       |
| Cost Allocation Tags | Track by team/app    | Detailed cost reporting |
| Organizations        | Consolidated billing | Multiple accounts       |

### Mnemonic

**See Cost → Cost Explorer**
**Limit Cost → Budgets**
**Group Cost → Tags**
**One Bill → Organizations**

---

## Migration

| Service                       | Memory Hook             | Use When You See    |
| ----------------------------- | ----------------------- | ------------------- |
| Application Discovery Service | Assess before migration | Inventory workloads |
| Application Migration Service | Move servers            | Lift-and-shift      |
| Migration Hub                 | Track migrations        | Central dashboard   |
| DataSync                      | Move files              | Storage migration   |

---

# High-Frequency Exam Keywords

These appear repeatedly in your question bank:

| Keyword in Question          | Answer Usually        |
| ---------------------------- | --------------------- |
| Audit / Who deleted resource | CloudTrail            |
| Vulnerability assessment     | Inspector             |
| Threat detection             | GuardDuty             |
| Sensitive data in S3         | Macie                 |
| Temporary credentials        | STS                   |
| EC2 access to AWS services   | IAM Role              |
| Cost alerts                  | Budgets               |
| Cost analysis                | Cost Explorer         |
| One bill for many accounts   | Organizations         |
| Infrastructure as Code       | CloudFormation        |
| Code using Python/Java/TS    | AWS CDK               |
| Relational database          | RDS                   |
| NoSQL                        | DynamoDB              |
| Serverless compute           | Lambda                |
| Containers without servers   | Fargate               |
| Dedicated connection         | Direct Connect        |
| Huge data migration          | Snowball / Snowmobile |
| Hybrid storage               | Storage Gateway       |

---

# 30-Second Memory Map

**Compute:** EC2, Lambda, Fargate, Beanstalk
**Storage:** S3, EBS, EFS, FSx, Glacier
**Database:** RDS, Aurora, DynamoDB, Redshift
**Security:** IAM, GuardDuty, Inspector, Macie, CloudTrail
**Network:** Route53, CloudFront, Direct Connect, Transit Gateway
**Cost:** Budgets, Cost Explorer, Organizations
**Migration:** Snowball, DataSync, Migration Hub, Storage Gateway

If you memorize just this one-page mapping, you'll be able to answer a large percentage of the service-identification questions in this CLF-C02 question bank.    
