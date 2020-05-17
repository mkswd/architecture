# Determine workload requirements

## Overview

One of the first things is to determine what are the requirements of your solution. Starting from the understanding of the business goals and what are the requirements that will guide the design to achieve them towards what is expected within the company.

### Define Business Objectives

- What is the purpose of this solution?
- Is this a 24x7 application?
- What RPO/RTO is acceptable?
- Does the application need to be globally available?

### Workloads

- Does your solution have more than one workload? Have you decomposed them?
- Is there, for each one, different requirements for availability, scalability, data consistency, or disaster recovery?

### Define, and Document, SLA and Cloud Metrics

- What is that availability customers will expect? 99.9? 99.99%?
- Define:
    - Service Agreement Level (SLA)
    - Mean Time To Recovery (MTTR)
    - Mean Time Between Failures (MTBF)
    - Recovery Point Objective (RPO)
    - Recovery Time Objective (RTO)

### Requirements: functional  and non-functional 

- Functional defines whether the application does the right thing.
- Nonfunction lets you define whether the application does those things well.

### Planning: Growth

- What are the expected users?
- How will you scale beyond that?

### Cost Management

- What is the strategy for costs?
- How to monitor then?
- Is there a plan for shared costs?
- Define a consumption optimization strategy


## 1. Requirements
In this design definition, it's important to identify all requirements for the solution.
It may happen that a solution does not have all of them, due to time pressure, company maturity, etc.
But it's important as an architect, to identify them and address them as much as possible.

### 1.1 Compliance

As an architect, we need to understand a company's compliance obligation and ensure the solution follows them.

- Understand the shared responsibility model
- Identify Compliance requirements
    - Policies
    - Standards (ISO 27001, CSA, SOC2)
    - Laws (GDPR, HIPAA, WCAG)
- Identify identity and access management (IAM) requirements
- Identify service-oriented architecture (SOA) requirements
    - How services are discovered?
    - Which design patterns to follow?
        - Event-drive?
        - Message-drive?
        - Containerization?
        - Stateful or Stateless?
    - How services integrate?

### 1.2 Accessibility

- Web Content Accessibility Guidelines (WCAG)
- Is it a law in our country?

### 1.3 Availabitity

- SLA dependency mapping
- Identify single points of failure

### 1.4 Capacity and Scalability

- How many users will use it?
- How much data will be transferred?
- How should scale when this increase/decrease?
- Does the workload already exist (Migration)? Is the assessment possible?
- PaaS? IaaS?
- Does scaling need to be handled via code?

### 1.5 Deploy-ability

- What are the environments? (Dev, State, etc..)
- Which toolset? (Repository, specific tools)
- How to CI?
- How to CD?

### 1.6 Configurability

- How the application will be configured?
- How to support different environments?
- PaaS: App variables, Deployment slots?
- Containers: Environment variables?
- Where to store secrets? key? certificates?

### 1.7 Governance

- How to control only authorized changes?
- Which policies to apply?
- "Only pipelines touches production" strategy? also for dev?

### 1.8 Maintainability

- How to enforce code level maintainability?
- How Logs should be handled?
- Which metrics should be monitored?
- How to handle bugs in a timely fashion way?

### 1.9 Security

- How to handle authentication?
- How to handle authorization?
- SSO, Federation?
- Attack detection? protection strategy?
- What does the code need to handle?
- Is there a security impact from a dependency?

### 1.10 Sizing

- Which resources to be used (compute)? How much is needed?
- Which are the pricing models?
- How to monitor them? how to respond to it?

### 1.11 Change Request

- How to handle change requests?
- How to incorporate changes during the project? and after?
- How to handle execution?
- Which standard will be used? TOGAF? ITIL?

### 1.12 Workload Dependency

- Does dependency mapping exist?
- Which products and services will be used?
- How to integrate with them?
- What are the impacts?

### 1.13 Testing

- Can tests be automated? 
- If not, will a manual test be the major part?
- Which test strategy to be implemented?
- Which test practices to be applied? Shift-left? Shift-right?
- Does a culture mind-shift necessary?

