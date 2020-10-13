# Design a Data Plataform solution

## Define key Metrics

- RPO
- RTO

## Defining Data Storage strategy

- Define the types of data

### Types of data

 - Data structure point of view

Structured
Semi-structured
Unstructured

- Management point of view

Managed
Unmanaged

- Data relation point of view

Relational 
Non-Relational

- Processing point of view

Online Transaction Processing (OLTP)
Online Analytical Processing (OLAP)




## Defining Auditing strategy

Define audit levels strategy

- Server level
- Database level

Define metrics and monitoring tool

## Defining Caching strategy

### Which type to use?

Private Caching
Used when data is held locally on the instance that is running the application or service. 

Shared Cache
Common source that can be access by multiple application processes and/or machines.

### Important definitions 

- When to?
- How to?
- Data expiration?
- Client-side cache invalidation?

## Define Data Retention Strategy

- Choose redundancy (geo)
- Choose retention policies (daily, weekly, yearly)

## Distributed Database Services

Define Consistancy Levels

Strong
Bounded Staleness
Session
Consistent  Prefix
Eventual

Solutions on Azure
Cosmos DB

## Define IoT strategy

## Define Big Data strategy

Solutions on Azure
SQL Data Warehouse
HDInsight
Data Lake Analytics
Azure Data Fabric
Azure Analysis Service

## Using Storage Services

### Types

- Blob Storage
- SMB File Storage
- Table Storage
- Queue Storage
- Disk Storage

### Storage tiers

Hot
Cold
Archive

### Managing Access

Shared Access Signature

## Defining Secrets Storage


## Define Price model

- Pay as you Go
- DTU
- RU

## Define Data Protection strategy

- Geo-Replication

- Encryption
Transparent Data Encryption (TDE)
Always Encrypted
Dynamic Data Masking
Encrypted in Transit (TLS/SSL)

- Scaling

- Security
Network level Security
Firewall
Auth
Row Level Security
Threat Protection


- Data Loss Prevention (DLP)

Identify sensitive data
Which standards to apply? (PII, PCI)
Define policies
Key encription (or Hash?)
Define data controller and processor (GDPR)

## Define Monitoring Strategy 
