# ☁️ Cloud Computing Fundamentals

Welcome to my study notes on Cloud Computing! This document covers the foundational concepts I explored during my first-day internship task at **Codomax**, including cloud service models, infrastructure layout, and virtualization.

---

## 1. Cloud Computing Service Models

Cloud services are categorized into three primary models, depending on the level of control and management required:

| Model | Full Form | What it Provides | User Manages | Provider Manages | Examples |
|-------|-----------|------------------|--------------|------------------|----------|
| **IaaS** | Infrastructure as a Service | Virtualized computing resources over the internet. | OS, Middleware, Runtime, Data, Applications | Virtualization, Servers, Storage, Networking | AWS EC2, Google Compute Engine, Azure VMs |
| **PaaS** | Platform as a Service | Hardware and software tools deployed over the internet, typically for application development. | Data, Applications | OS, Middleware, Runtime, Servers, Storage, Networking | Heroku, Google App Engine, AWS Elastic Beanstalk |
| **SaaS** | Software as a Service | Fully functional software applications delivered over the internet on a subscription basis. | Nothing (just user configuration) | Everything (Infrastructure to Application) | Gmail, Microsoft 365, Salesforce, Dropbox |

---

## 2. Cloud Regions and Availability Zones

To ensure high availability, fault tolerance, and low latency, cloud providers organize their infrastructure geographically:

- **Cloud Region**: A physical geographic location (e.g., `us-east-1`, `eu-west-1`) where a cluster of cloud data centers is hosted. Choosing a region close to your end-users reduces latency and helps meet data residency/compliance requirements.
- **Availability Zone (AZ)**: One or more discrete, physically separate data centers *within* a Region. Each AZ has independent power, cooling, and networking. 
  - *Best Practice*: Deploying applications across multiple AZs within a region protects against localized failures (e.g., power outage in one data center) and ensures high availability.

---

## 3. Virtualization

**Virtualization** is the foundational technology that makes cloud computing possible. 

- **What it is**: The process of creating a software-based (virtual) representation of something, such as virtual machines (VMs), storage, or networks, rather than physical hardware.
- **How it works**: A software layer called a **Hypervisor** (e.g., VMware ESXi, KVM, Hyper-V) sits between the physical hardware and the virtual machines. It abstracts the physical resources and allocates them dynamically to multiple isolated VMs.
- **Benefits**:
  - **Resource Efficiency**: Multiple OS environments can run on a single physical server.
  - **Isolation**: If one VM crashes, it does not affect others on the same host.
  - **Scalability & Flexibility**: New VMs can be provisioned in minutes.

---

## 4. Key Takeaways
- **IaaS** gives you the building blocks, **PaaS** gives you a development environment, and **SaaS** gives you a finished product.
- Always design for failure by utilizing multiple **Availability Zones** within a **Region**.
- **Virtualization** is the magic behind the cloud, enabling efficient, scalable, and isolated resource allocation.

---
*Author: Dhanusha*  
*3rd Year BSc Computer Science | Intern at Codomax*  
*Last Updated: November 2026*