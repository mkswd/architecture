# Design for Identity and Security

## 1. Design Identity Management

- Filtering
- Password hash synchronization
- Password writeback
- Device writeback
- Accidental deletes prevention
- Automatic Upgrade
- Self Service

## 2. Design Authentication

### 2.1 Authentication Mechanisms

- User ID and password auth
- Federation 
- Single Sign-ON (SSO)

### 2.2 Authentication Methods

- Cloud-Only
- Password Hash Sync + Seamless SSO (Hybrid)
- Pass-Through Authentication (Hybrid)
- Federation 
- Federation with Password hash Sync 

### 2.3 How to choose the right method?

![Decition Tree](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/media/choose-ad-authn/azure-ad-authn-image1.png)

### 2.3 Security

- IPSec 
    - Authentication Headers (AH)
    - TLS/SSL
- Multi-factor Authentication
    - methods
    - register process
    - implementation strategy

## 3. Design Authorization

- Define Access levels
- Define granularity
- Credential checkpoints

### 3.1 Topics to consider

- Impersonation/ Delegating of authentication
- Role-based Access Control

### 3.2 Security

- Conditional Access
- Secret Holding Delegation

## 4. Design Risk Prevention for Identity

- Risk mapping
- Catalog Frequency and Size
- Define Patching strategy

### 4.1 Risk Factors to consider

- Financial Costs
- Data Loss
- Denial of Service (DoS)
- Image Risk (Loss of Trust
- Customer Confidence Impact
- Government and Corporate Compliance

### 4.2 Common risk causes

- Expired users
- High permission
- Physical access

### 4.3 Mesures

- Access Reviews
- Least Privilege principle
- Policies 
- Health Checks
- Compliance to standards
- Training
- Layers of Security
- Toolset: Firewall/antivirus
- *Advanced threat Protection (ATP)

### 5. Design Monitoring Strategy for Identity and Security

- Define Metrics
- Alert/Notification strategy
- Privileged Identity Management (PIM)

### 5.1 Securing Privileged (PIM) Access Roadmap

![Roadmap](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/media/directory-admin-roles-secure/roadmap-timeline.png)

- Stage 1 (24-48 hours): Critical items that we recommend you do right away
- Stage 2 (2-4 weeks): Mitigate the most frequently used attack techniques
- Stage 3 (1-3 months): Build visibility and build full control of admin activity
- Stage 4 (six months and beyond): Continue building defenses to further harden your security platform

[click here for more details about the stages](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-admin-roles-secure)