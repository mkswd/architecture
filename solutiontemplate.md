# Cloud Solution Architecture Design Document

Here is a checklist for cloud architecture to guide, not just decision making, but most important, documentation:

[Reference architectures](https://docs.microsoft.com/en-us/azure/architecture/architectures/?filter=reference-architecture) <br>
[Design principles](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/) <br>
[Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/) <br>
[Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices) <br>

## <ins>0. Overview

Describe the application and it's goal

## <ins>1. Architecture style

Describe architecture style chose.

[N Tier](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier) <br>
[Web-Queue-Worker](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/web-queue-worker) <br>
[Microservices](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/microservices) <br>
[Event-driven architecture](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/event-driven) <br>
[Big Data](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data) <br>
[Big Compute](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-compute) <br>


### 1.1 Dependency Management

Describe the dependy management brought by the architecture style chose.

|Architecture style	| Dependency management	| Domain type |
|-|-|-|
|N-tier |	Horizontal tiers divided by subnet	Traditional business domain | Frequency of updates is low |
|Web-Queue-Worker |	Front and backend jobs, decoupled by async messaging |	Relatively simple domain with some resource intensive tasks |
|Microservices |	Vertically (functionally) decomposed services that call each other through APIs |	Complicated domain. Frequent updates |
|Event-driven architecture |	Producer/consumer. Independent view per sub-system |	IoT and real-time systems
|Big data |	Divide a huge dataset into small chunks. Parallel processing on local datasets.	Batch and real-time data analysis | Predictive analysis using ML |
|Big compute |	Data allocation to thousands of cores |	Compute intensive domains such as simulation|

### 1.2 Domain type
Traditional business domain with low frequency of updates (releases are done once per month)

### 1.3 Benefits

Describe the benefits from the solution

### 1.4 Challenges

Describe the challanges for the chose architecture. For example:

* Complexity
* Asynchronous messaging and eventual consistency
* Inter-service communication
* Manageability

### 1.5 Best Practices

* Auto scaling to handle changes in load (VM scale sets are high recommended for this architecture style)
* Cache semi static data
* Database tier with high availability
* Web Application Firewall (WAF) between Front-end and internet
 
## <ins>2. Technology Choices
### 2.1 Compute

Describe compute chosing and reasons.

![Compute Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/images/compute-decision-tree.svg)

### 2.2 Data

Describe data chosing and reasons.

#### 2.2.1 Application Data

Specific topic for application data.

#### 2.2.2 Application Logs

Specific topic for application logs.

#### 2.2.1 Sensitive Information and Personal Identifiable Information (PI)I

Specific topic for securing personal  

### 2.3 Load balancing

Describe load balacing chosing, reasons and details.

- Global vs regional 
- HTTP(S) versus non-HTTP(S)

Options on Azure: 

- Front Door
- Traffic Manager
- Application Gateway
- Azure Load balancer

![Data Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/images/load-balancing-decision-tree.png)

### 2.3 Messaging

Describe load balacing chosing, reasons and details.

Options on Azure:

- Azure Service Bus
- Azure Event Grid
- Azure Event Hubs

Related Pattenrs:

- [Competing Consumers Pattern.](https://docs.microsoft.com/en-us/azure/architecture/patterns/competing-consumers)
- [Priority Queue Pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/priority-queue)
- [Queue-based Load Leveling Pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/queue-based-load-leveling)
- [Retry Pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/retry)
- [Scheduler Agent Supervisor Pattern.](https://docs.microsoft.com/en-us/azure/architecture/patterns/scheduler-agent-supervisor)
- [Choreography pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/choreography)
- [Claim-Check Pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/claim-check)

## <ins>3. Application Architecture

Describe the technical details about your architecture with diagrams. For example:

[4+1 View Model](https://dev.azure.com/NextGuestDevLab/NextGuestCRM/_wiki/wikis/NextGuestCRM.wiki/114/4-1-View-Model) <br>
[C4 Model](https://dev.azure.com/NextGuestDevLab/NextGuestCRM/_wiki/wikis/NextGuestCRM.wiki/115/C4-Model).

### 3.1 Tech stack

Describe your tech stack.

# <Solution Name> Architecture Implementation

A successful cloud application will focus on five tenets to design a solution: Cost, DevOps, resiliency, scalability and security.
To guide us on how to improve the quality of our workloads we're using Azure Well-Architected Framework. Here you can find the design decisions made <Application Name>.
<br>

Pillar | Description
- | -
Cost|	Managing costs to maximize the value delivered.
Operational Excellence |	Operations processes that keep a system running in production.
Resiliency|	The ability of a system to recover from failures and continue to function.
Scalability|	The ability of a system to adapt to changes in load.
Security|	Protecting applications and data from threats.

## <ins>1. Cost

Describe the cost monitoring design

## <ins>2. Operational Excellence (DevOps)

Describe your CI/CD strategy. 
Include building, stamp (if exist), relase, artificats building, etc.

Also:

- Instrumentation. Generating the raw data, from application logs, web server logs, diagnostics built into the Azure platform, and other sources.
- Collection and storage. Consolidating the data into one place.
- Analysis and diagnosis. To troubleshoot issues and see the overall health.
- Visualization and alerts. Using telemetry data to spot trends or alert the operations team.

[DevOps Checklist](https://docs.microsoft.com/en-us/azure/architecture/checklist/dev-ops)

## <ins>3. Resiliency

Describe the resiliency (embrace failure!) strategy.

## <ins>4. Scalability

Describe the scalability strategy

## <ins>5. Security
This section will define how Security is designed for this solution and it's role in this project. Since this is a lift-and-shift project, a [Shared Responsibility model](https://docs.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility) is implicit chose as guide to you security strategy.

![Security Model](https://docs.microsoft.com/en-us/azure/security/fundamentals/media/shared-responsibility/shared-responsibility.png "Responsibility zones")

### 5.1 Identity Management
*To be described* 
Governance, risk and Compliance

### 5.2 Infrasctrucure Security
*To be described*

### 5.3 Application Security
*To be described*

### 5.4 Data sovereignty and encryption
*To be described*
