# Cloud Computing Notes

## Table of Contents
- [Service Models](#service_models)
- [Deployment Models](#deployment_models)
- [Cloud Infrastructure](#cloud_infrastructure)
- [Resources](#resources)

<a id="service_models"></a>
## Service Models
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### (SaaS) Software-as-a-Service
- **Complexity:** Low
- **Description:** Software distribution model where applications are hosted by a third-party provider and made available to customers over the internet.
- **Common Use Cases:** Email, calendar, office tools (like Microsoft Office 365), and CRM (Customer Relationship Management) systems.
- **Benefits:** 
  - Easy accessibility, centrally managed.
  - Automatic updates and patch management.
  - Subscription-based models - pay only for what you use.

### (PaaS) Platform-as-a-Service
- **Complexity:** Medium
- **Description:** Provides a platform allowing customers to develop, run, and manage applications without the complexity of building and maintaining the infrastructure.
- **Common Use Cases:** Application development, middleware, and database management.
- **Benefits:** 
  - Simplified process for developing and deploying apps.
  - Scalable solutions with support for a diverse array of programming languages.
  - Reduced costs and complexity with the underlying infrastructure managed by the provider.

### (IaaS) Infrastructure-as-a-Service
- **Complexity:** High
- **Description:** Delivers fundamental computing resources (such as compute, network, and storage) to consumers on-demand, over the internet, in a pay-as-you-go model.
- **Common Use Cases:** Website hosting, backup and recovery, and high-performance computing without the physical hardware constraints.
- **Components:**
  - (VM) Virtual Machine
  - Storage
  - Network (like firewalls and other communication components)
- **Benefits:** 
  - Improved scalability and flexibility.
  - Only pay for what you use, helping to reduce costs.
  - Control over the infrastructure without the physical maintenance of hardware.

<!-- /MarkdownTOC -->
</details>

---

<a id="deployment_models"></a>
## Deployment Models
<details close>
<summary><b>(click to expand/hide)</b></summary>

<!-- MarkdownTOC -->

### Public Cloud
- **Description:** Computing services offered by third-party providers over the public Internet, making them available to anyone who wants to use or purchase them.
- **Characteristics:**
  - Services available to multiple clients using shared infrastructure.
  - Scalable, on-demand resources.
- **Use Cases:** Web-based email, online office applications, storage.
- **Benefits:**
  - Reduced costs and maintenance.
  - High reliability.
  - Scalability.

### Private Cloud
- **Description:** Computing resources used exclusively by one business or organization. The private cloud can be physically located at your organization's on-site datacenter or hosted by a third-party service provider.
- **Characteristics:**
  - Exclusive resource use, often on-premises.
  - Enhanced security controls.
- **Use Cases:** Companies with strict data, regulatory, and governance requirements.
- **Benefits:**
  - Increased security and privacy.
  - Customization.
  - Consistent performance.

### Hybrid Cloud
- **Description:** A mix of public and private cloud environments, with orchestration between the two. Businesses can run mission-critical workloads or sensitive applications on the private cloud while using the public cloud for workloads that must scale on-demand.
- **Characteristics:**
  - Combination of private and public cloud resources.
  - Flexibility and scalability.
- **Use Cases:** Businesses with variable workloads and data processing needs.
- **Benefits:**
  - Versatility.
  - Cost management.
  - Enhanced performance.

### Community Cloud
- **Description:** A cloud infrastructure shared by several organizations with common concerns, ensuring security, compliance, and policy requirements. It can be managed by the organizations or a third party and can exist on or off-premises.
- **Why Use Community Cloud?:** Provides a secure, shared environment for organizations with common goals or tasks. Offers the same set of security controls and supports data localization requirements.
- **Modern Approach - Software-Defined Community Cloud:** Google Cloud's software-defined community cloud separates shared projects from others, providing enhanced security and compliance without physical infrastructure limitations. It enables faster access to new services and security enhancements, ensuring improved efficiency and performance.
- **Benefits:** Meets specific community security and compliance requirements, allows quicker onboarding of new technologies, and enhances availability and efficiency due to scalable infrastructure.


<!-- /MarkdownTOC -->
</details>

---

<a id="cloud_infrastructure"></a>
## Cloud Infrastructure
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### Region 
- **Description:** is a geographic area or location where a Cloud provider's infrastructure is clustered, and may have names like **NA South** or **US East**.

#### Availability Zones (AZ)
- **Description:** Each cloud region can have multiple Zones and (data centers) have their own power, cooling, networking resources and may have names like **US-East-1** or **DAL-09**
- **Benefits:**
  - Isolation of zones improves the cloud's fault tolerance, decreases latency, and more.
  - Very high bandwidth connectivity with other AZs, Data Centers and the internet.

#### Cloud Data Center
- **Description:** is a huge room or a warehouse containing cloud infrastructure (pods and racks, or standardized containers of computing resources such as servers, storage and networking equipment)

#### Computing Resources

- **Servers:**
  - Virtual Machines: Emulated computers based on physical servers.
  - Bare Metal Servers: Physical servers without layers of virtualization.
  - Serverless: On-demand computing execution with zero server management.

- **Storage:**
  - Associated with both virtual and physical servers.

- **Networking:**
  - **Infrastructure Components:**
    - Routers and switches form the backbone of cloud networking.
  
  - **Advantages:**
    - Simplified networking tasks including provisioning, configuration, and management.
  
  - **Configuration Essentials:**
    - Requires setting up IP addresses and subnets.
  
  - **Security Configurations:**
    - Vital to manage access to resources via security groups, ACLs, VLANs, VPCs, and VPNs.
  
  - **Virtualized Networking Hardware:**
    - Appliances like firewalls, load balancers, gateways, and traffic analyzers are available as virtual services.
  
  - **Enhanced Delivery:**
    - Cloud providers offer Content Delivery Networks (CDNs) for improved and accelerated web content delivery.

---

#### Virtualization and Virtual Machines

##### Introduction
- **Presenter:** Kaleigh Bovey from the IBM Cloud team
- **Topic:** Overview of virtualization in the context of cloud computing

##### What is Virtualization?
- **Definition:** The creation of a virtual (rather than actual) version of something, such as compute resources, storage, networking, servers, or applications.
- **Key Component:** Hypervisor

##### Hypervisors
- **Function:** Allows multiple operating systems to share a single hardware host.

##### Types of Hypervisors
1. **Type 1 Hypervisor**
   - Directly installed on physical server hardware.
   - Also known as a "bare-metal hypervisor."
   - Examples: VMware ESXi, Microsoft Hyper-V, KVM.
   - Characteristics: High security, lower latency, commonly used in enterprise environments.

2. **Type 2 Hypervisor**
   - Installed on a host operating system.
   - Also known as "hosted hypervisor."
   - Examples: Oracle VirtualBox, VMware Workstation.
   - Characteristics: Higher latency, commonly used for end-user virtualization.

##### Virtual Machines (VMs)
- **Definition:** Software-based emulations of a computer system.
- **Features:**
  - Contains an operating system and applications.
  - Independent from one another.
  - Can run multiple instances on a single hypervisor.
  - Supports various operating systems (e.g., Windows, Linux, UNIX).
  - High portability.

##### Key Benefits of Virtualization
1. **Cost Savings:**
   - Reduces the need for physical infrastructure.
   - Saves on electricity, maintenance, and server costs.

2. **Agility and Speed:**
   - Quick to create and deploy VMs.
   - Simplifies processes such as dev-test scenarios.

3. **Reduced Downtime:**
   - VMs can be quickly moved to another hypervisor if a host fails, ensuring a reliable backup plan and continuous system operation.

##### Conclusion
- Virtualization is central to cloud computing, offering numerous benefits in efficiency, cost savings, and agility.
- **Next Topic Preview:** Discussion of various types of virtual machines in the following session.

---

#### Overview of Virtual Machines in Cloud Computing

##### Introduction
- **Topic:** Various types and characteristics of Virtual Machines (VMs) in cloud environments.

##### Virtual Machines (VMs)
- Also known as Virtual Servers, Virtual Instances, or simply "instances."
- Available in multiple configurations for diverse use cases.
- **Deployment Specifications:**
  - Selection of Region, Zone, or Data Center.
  - Choice of Operating System.
- **Billing Options:** Hourly or monthly.
- **Infrastructure Options:** Shared (multi-tenant) or dedicated (single-tenant).

##### Types of VMs

##### 1. Shared/Public Cloud VMs
- Multi-tenant, provider-managed VMs.
- Provisioned on-demand with predefined or custom sizes.
- Configurations for various workloads (Compute Intensive, Memory Intensive, High Performance I/O).
- Priced per hour or month.
- **Use Cases:** General purpose applications, development environments.

##### 2. Transient/Spot VMs
- Lower-cost VMs utilizing unused cloud data center capacity.
- Subject to de-provisioning by the provider

---

### Overview of Virtual Machines in Cloud Computing

#### Introduction
- **Topic:** Various types and characteristics of Virtual Machines (VMs) in cloud environments.

#### Virtual Machines (VMs)
- Also known as Virtual Servers, Virtual Instances, or simply "instances."
- Available in multiple configurations for diverse use cases.
- **Deployment Specifications:**
  - Selection of Region, Zone, or Data Center.
  - Choice of Operating System.
- **Billing Options:** Hourly or monthly.
- **Infrastructure Options:** Shared (multi-tenant) or dedicated (single-tenant).

#### Types of VMs

##### 1. Shared/Public Cloud VMs
- Multi-tenant, provider-managed VMs.
- Provisioned on-demand with predefined or custom sizes.
- Configurations for various workloads (Compute Intensive, Memory Intensive, High Performance I/O).
- Priced per hour or month.
- **Use Cases:** General purpose applications, development environments.

##### 2. Transient/Spot VMs
- Lower-cost VMs utilizing unused cloud data center capacity.
- Subject to de-provisioning by the provider at any time.
- **Use Cases:** Non-critical applications, testing, stateless workloads, big data, high-performance computing (HPC) tasks.

##### 3. Reserved Instances
- Capacity reservation for a specified term (1 year, 3 years, etc.).
- Guarantees resource availability.
- Reduced costs compared to standard instances.
- **Use Cases:** Long-term projects, steady-state workloads, financial forecasting benefits.

##### 4. Dedicated Hosts
- Single-tenant VMs ensuring privacy and control.
- Exclusive use of the host’s resources.
- Placement control over workloads.
- Compliance with regulatory requirements and specific licensing terms.
- **Use Cases:** Data-sensitive tasks, compliance-restricted workloads, performance-intensive applications.

#### Conclusion
- VMs are fundamental components in cloud computing, offering versatility for a wide range of use cases.
- They deliver various benefits, including cost efficiency, scalability, and strategic performance allocation.

---

<!-- /MarkdownTOC -->
</details>

---

<a id="resources"></a>
## Resources
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- []()

<!-- /MarkdownTOC -->
</details>

---
