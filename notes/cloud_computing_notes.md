# Cloud Computing Notes

## Table of Contents
- [Service Models](#service_models)
- [Deployment Models](#deployment_models)
- [Cloud Infrastructure](#cloud_infrastructure)
- [Cloud Storage and Content Delivery Networks](#storage_and_delivery_networks)
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
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- **Description:** is a geographic area or location where a Cloud provider's infrastructure is clustered, and may have names like **NA South** or **US East**.

<!-- /MarkdownTOC -->
</details>

### Availability Zones (AZ)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- **Description:** Each cloud region can have multiple Zones and (data centers) have their own power, cooling, networking resources and may have names like **US-East-1** or **DAL-09**
- **Benefits:**
  - Isolation of zones improves the cloud's fault tolerance, decreases latency, and more.
  - Very high bandwidth connectivity with other AZs, Data Centers and the internet.

<!-- /MarkdownTOC -->
</details>

### Cloud Data Center
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- **Description:** is a huge room or a warehouse containing cloud infrastructure (pods and racks, or standardized containers of computing resources such as servers, storage and networking equipment)

<!-- /MarkdownTOC -->
</details>

### Computing Resources
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

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

<!-- /MarkdownTOC -->
</details>

---

### Virtualization and Virtual Machines
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

#### Introduction
- **Presenter:** Kaleigh Bovey from the IBM Cloud team
- **Topic:** Overview of virtualization in the context of cloud computing

#### What is Virtualization?
- **Definition:** The creation of a virtual (rather than actual) version of something, such as compute resources, storage, networking, servers, or applications.
- **Key Component:** Hypervisor

#### Hypervisors
- **Function:** Allows multiple operating systems to share a single hardware host.

#### Types of Hypervisors
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

#### Virtual Machines (VMs)
- **Definition:** Software-based emulations of a computer system.
- **Features:**
  - Contains an operating system and applications.
  - Independent from one another.
  - Can run multiple instances on a single hypervisor.
  - Supports various operating systems (e.g., Windows, Linux, UNIX).
  - High portability.

#### Key Benefits of Virtualization
1. **Cost Savings:**
   - Reduces the need for physical infrastructure.
   - Saves on electricity, maintenance, and server costs.

2. **Agility and Speed:**
   - Quick to create and deploy VMs.
   - Simplifies processes such as dev-test scenarios.

3. **Reduced Downtime:**
   - VMs can be quickly moved to another hypervisor if a host fails, ensuring a reliable backup plan and continuous system operation.

#### Conclusion
- Virtualization is central to cloud computing, offering numerous benefits in efficiency, cost savings, and agility.
- **Next Topic Preview:** Discussion of various types of virtual machines in the following session.

<!-- /MarkdownTOC -->
</details>

---

### Overview of Virtual Machines in Cloud Computing
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

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

<!-- /MarkdownTOC -->
</details>

---

### Bare Metal Servers in Cloud Computing
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

#### Definition
- **Bare Metal Server:** A single-tenant, dedicated physical server dedicated to a single customer.

#### Key Features
- **Management by Cloud Provider:** The provider handles the server up to the OS. They ensure the hardware and rack connections are functional.
- **Customer's Responsibility:** Administration and management above the OS level.
- **Configuration Options:** Pre-configured by the provider or custom-configured based on customer's specifications.
- **Additional Features:** GPUs for tasks like scientific computation, data analytics, and professional virtual graphics.

#### Provisioning and Costs
- **Provisioning Time:** 
  - Preconfigured builds: 20-40 minutes.
  - Custom builds: 3-4 hours.
  - Times vary by cloud provider.
- **Cost:** Generally more expensive than VMs due to dedicated usage.
- **Availability:** Not all cloud providers offer bare metal servers.

#### Use Cases and Advantages
- Suitable for high-performance, highly secure, and isolated environments.
- **Performance:** Meets the demands of high-performance computing (HPC) and data-intensive applications.
- **Workload Examples:** ERP, CRM, AI, deep learning, virtualization, big data analytics, and GPU-intensive tasks.
- **Security & Control:** Full customer access without needing a hypervisor; ideal for applications needing high security control.

#### Bare Metal vs. Virtual Servers
- **Bare Metal Advantages:**
  - Best for CPU and I/O intensive workloads.
  - Highest performance and security.
  - Satisfies strict compliance requirements.
  - Complete flexibility, control, and transparency.
  - Comes with added management and operational overhead.
- **Virtual Servers Advantages:**
  - Rapid provisioning.
  - Elastic and scalable.
  - Lower cost.
  - Limitations in performance and throughput due to shared hardware.

#### Conclusion
- **Bare Metal Servers:** Ideal for high-performance and security-centric applications.
- **Virtual Servers:** Best for quick, scalable, and cost-effective solutions.

<!-- /MarkdownTOC -->
</details>

---

### Secure Networking In Cloud
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

#### Introduction
- The surge in **Cloud adoption** and **cybersecurity threats** necessitates robust Cloud network security.
- Cloud networks mimic on-premises networks but use logical instances (e.g., vNICs) instead of physical hardware.

#### Building a Cloud Network
##### 1. Initiation:
   - Define the network size or IP address range.
   - Deploy in logically separated segments with Virtual Private Clouds (VPCs) and sub-divisions known as subnets.

##### 2. Utilization of Subnets:
   - Cloud resources (VMs, storage, etc.) are deployed into these subnets.
   - Allows for multi-tier concepts familiar from on-premises setups.
   - Crucial for implementing security measures.

##### 3. Security Implementation:
   - Subnets are shielded with access control lists (ACLs), acting as firewalls.
   - Further instance-level security with security groups.

##### 4. Application Deployment:
   - Set up different security groups for different types of VSIs (e.g., Web access, application tier, database).
   - Implement public gateway instances for internet-facing applications.

##### 5. Connectivity Enhancements:
   - Extend on-premises resources securely using Virtual Private Networks (VPNs).
   - Maintain application responsiveness with load balancers.
   - For hybrid Cloud environments, utilize dedicated connections (like IBM's Direct Link) for improved security and efficiency.

#### Conclusion
- Constructing a Cloud Network involves creating logical structures providing functionalities similar to traditional data center networks, crucial for securing digital environments and ensuring efficient application performance.

<!-- /MarkdownTOC -->
</details>

---

### Containers
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

#### Introduction

- Containers package application code, libraries, and dependencies into a single unit to run consistently across environments.
- They are lightweight compared to VMs, requiring no guest OS.

#### History of Containerization

- Originated in 2008 with Linux kernel introducing control groups (Cgroups).
- Paved the way for Docker, Cloud Foundry, Rocket, etc.

#### Containers vs. Virtual Machines (VMs)

- VMs include the application, necessary binaries, libraries, and an entire guest OS for each instance, consuming substantial system resources.
- Containers share the host OS and include only the app and its dependencies, making them more efficient.

##### Problems with VMs:

1. **Resource-Intensive**: Each instance of VM needs a full-blown OS, consuming significant system resources.
2. **Scaling Issues**: Scaling requires duplicating the whole VM, further using up system resources.
3. **Compatibility Issues**: Applications may run on a developer’s machine but face compatibility issues when transferred to a VM.

#### Containerization Process

- Starts with a manifest (e.g., Dockerfile).
- Creation of an image (e.g., Docker image).
- Deployment of the container.

#### Advantages of Containerization

1. **Efficiency**: Containers are lightweight and share the host’s OS kernel, avoiding the overhead of running entire OS instances.
2. **Scalability**: Easier to scale out because of their smaller size.
3. **Consistency across Environments**: Runs the same, regardless of where they are deployed.
4. **Resource Distribution**: Unused resources by one container can be utilized by others, optimizing resource use.
5. **Microservices**: Ideal for a microservices approach, allowing different services to be deployed, maintained, and scaled independently.

#### Conclusion

- Containers facilitate cloud-native architectures, making development, deployment, and scaling more efficient and consistent.
- They enable agile DevOps practices and continuous integration and delivery (CI/CD).

<!-- /MarkdownTOC -->
</details>

---

<!-- /MarkdownTOC -->
</details>

---

<a id="storage_and_delivery_networks"></a>
## Cloud Storage and Content Delivery Networks
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### Basics of Storage on Cloud
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Introduction
Cloud storage involves saving data to an off-site storage system maintained by a third party. It allows for scalability, flexibility, and accessibility, with pricing based on the storage used.

## Types of Cloud Storage

### Direct Attached Storage (DAS)
- **Description**: Storage directly connected to a cloud server, often within the same physical enclosure.
- **Characteristics**:
  - High speed due to proximity.
  - Primarily used for operating systems.
  - Ephemeral, tied to the lifespan of its compute node.
  - Not suitable for shared access across multiple systems.
- **Limitations**: Less resilient to failures, not ideal for long-term storage.

### File Storage (NFS)
- **Description**: Network-attached storage offering shared access to files.
- **Characteristics**:
  - Data accessible over standard ethernet networks.
  - Utilizes a familiar hierarchical structure.
  - Can be mounted by multiple servers.
- **Performance**: Slower than DAS and Block storage, cost-effective.

### Block Storage
- **Description**: High-speed, highly reliable storage suitable for databases and intensive applications.
- **Characteristics**:
  - Accessed through high-speed fibre connections.
  - Provisioned in volumes and seen as individual hard drives by compute nodes.
  - Supports a single compute node at a time.
- **Performance**: Fast read/write capabilities. Associated term: 'IOPS' (Input/Output Operations Per Second).

### Object Storage
- **Description**: Accessed via API, suitable for a vast array of unstructured data.
- **Characteristics**:
  - Most affordable storage option.
  - Infinite scalability from the user perspective.
  - Data accessibility through direct calls to the object itself, not reliant on a compute node.
- **Usage**: Ideal for documents, media, backups, application data, and more.
- **Performance**: Slower read/write speeds compared to other storage types.

## Considerations in Cloud Storage

- **Persistence**: Refers to whether data remains stored even after its compute node is terminated. Persistent storage remains, whereas non-persistent (ephemeral) storage is deleted with its compute node.
- **Snapshots**:
  - Quick to create, recording only changes made after the previous snapshot.
  - Ideal for reverting systems to a previous state.
  - Not suitable for individual file recovery.

## Conclusion
Choosing the right type of cloud storage requires considering data accessibility, speed, resilience, and cost. Each storage type has its unique benefits suitable for specific use cases and applications.

<!-- /MarkdownTOC -->
</details>

---

### File Storage
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Detailed Overview of File Storage

## Characteristics of File Storage

- **Attachment**: Requires connection to a compute node for access and operation, similar to direct attached storage.
- **Cost and Maintenance**: Generally more cost-effective and resilient compared to direct attached storage, requiring less user intervention for disk management and maintenance.
- **Capacity**: Allows for provisioning of large storage quantities, presented as disks to servers.
- **Storage Appliances**: 
  - Disks are housed in specialized hardware separate from compute nodes.
  - High resilience and enhanced data security, with features like in-transit encryption.
  - Fully managed by service providers.

## Connectivity and Performance

- **Networking**:
  - Utilizes ethernet networks, often dedicated, for connecting storage to compute nodes.
  - Commonly known as 'Network Attached Storage' (NAS) or 'Network File Storage' (NFS).
- **Performance Variability**: 
  - Speed can fluctuate based on network load, impacting bandwidth.
  - Not suited for tasks requiring consistently high network speeds due to potential latency.

## Use Cases and Workload Suitability

- **Multi-Access Capability**: Can be mounted on multiple compute nodes simultaneously, appearing as an ordinary drive.
- **Ideal Applications**: 
  - Common/shared storage areas (e.g., departmental file shares, application processing zones, web service file repositories).
  - Contexts where network speed variability is non-critical.
- **Other Uses**: 
  - Viable for databases or other applications when budget constraints exist, with a trade-off in speed.

## IOPS Considerations in File Storage

- **Definition**: 'Input/Output Operations Per Second' - indicates the speed of data writing and reading on the disks (independent of network speed).
- **Cost Implication**: Higher IOPS usually implies increased expenses.
- **Significance**: 
  - Critical in matching storage performance with application demands.
  - Mismatched IOPS (too low) can slow down applications, whereas unnecessarily high IOPS may lead to overpayment.

## Example Scenario

- Scenario: A shared file storage used by 30 compute nodes, with an application performing 60 data operations per minute.
- Calculation: This equates to roughly 1 operation per second, illustrating the varying IOPS demands of different applications.

## Conclusion

Understanding the specifics of File Storage, including its connectivity, performance, and appropriate use cases, is crucial in leveraging its capabilities effectively. IOPS, a key performance metric, requires careful consideration to balance costs and maintain application efficiency.

<!-- /MarkdownTOC -->
</details>

---

### Block Storage
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Understanding Block Storage and Its Comparison with File Storage

Presenter: Amy Blea, IBM Cloud

## Introduction to Block Storage

- **Functionality**: Stores data in separate chunks or 'blocks', each with a unique address.
- **Accessibility**: Must be attached to a compute node to be functional, akin to direct attached storage and file storage.
- **Security and Resilience**: 
  - Mounted from remote storage appliances, offering high failure resilience.
  - Ensures data security through services like encryption during transit and while at rest.

## Connectivity and Performance of Block Storage

- **Network**: Utilizes a dedicated fiber optic network, enabling signal travel at light speed.
- **Cost and Efficiency**: 
  - More expensive due to high-speed fiber network construction, reflecting a higher price point.
  - Ideal for low-latency, high-performance workloads due to speed and consistency.

## Workloads and Suitability

- **Exclusive Access**: Typically mounted to a single compute node, unlike file storage that supports multiple nodes.
- **Ideal Workloads**: 
  - Perfect for consistent, high-speed storage demands (e.g., databases, mail servers).
  - Not suitable for scenarios requiring shared disk access among nodes.

## Understanding IOPS in Block Storage

- **IOPS Specification**: Cloud providers often allow IOPS characteristics specification during storage provisioning, adjustable according to application demands and behavior changes.

## Comparing Block and File Storage

- **Common Features**:
  - Both sourced from appliances managed by service providers.
  - High availability, resilience, and data encryption features.
- **Connectivity Differences**:
  - File storage uses ethernet (also called Network Attached or NFS Storage), susceptible to speed variability.
  - Block storage employs a consistent, high-speed fiber network.
- **Access Flexibility**:
  - File storage supports multiple compute node attachments simultaneously.
  - Block storage restricts attachment to one node at a time.
- **Use Case Based Selection**:
  - File storage: Preferred for non-speed-sensitive workloads, cost concerns, or necessary file sharing.
  - Block storage: Chosen for applications demanding fast, consistent disk access (e.g., databases).

## Deep Dive into Traditional Storage Types with IBM Cloud

- **Block Storage Overview**: 
  - Accessed by servers through a Storage Area Network (SAN).
  - Offers the lowest latency for applications, suitable for high-performance tasks.
  - Generally features high redundancy across volumes for data safety.

- **File Storage Specifics**:
  - Connects through a common network, supporting multiple server access.
  - Ideal for scalable situations with multiple file shares.
  - Allows multiple simultaneous reads/writes without data overwrite concerns.

- **Choosing Between Block and File Storage**:
  - **Block Storage is ideal for**:
    - Boot volumes for configurations like VMware.
    - Low latency and high-performance tasks (e.g., transactional/relational databases).
  - **File Storage is perfect for**:
    - Environments with mixed data types (e.g., web hosting servers).
    - Collaborative spaces needing concurrent access and operations.

- **Relevance**: Despite being traditional, both storage types maintain significant relevance due to their distinctive benefits for various workloads, whether on-premise or cloud-based.

## Conclusion and Further Discussion

- Both block and file storage continue to play critical roles in diverse workload management, each with unique strengths.
- Future topics will explore newer, cutting-edge storage solutions, including Object Storage.

**Feedback and Engagement**: Viewers are encouraged to comment, provide feedback, suggest topics, and subscribe for more insightful content.


<!-- /MarkdownTOC -->
</details>

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
