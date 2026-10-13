# Midterm Study Guide

The midterm exam will take the full class period on Thursday (10/15).
The exam will primarily consist of multiple-choice and multiple-select questions. Many questions will be scenario-based, so you should understand not only the definitions of cloud concepts and services, but also when and why you would use them.
Some questions will ask you to select one best answer, while others may ask you to select multiple correct answers. When multiple answers are required, the question will clearly indicate this.
The exam will be open book and open notes. You may use the course slides, course website, your own notes, assignments, and other course materials. However, the exam must be completed individually. You may not communicate or collaborate with other students during the exam.
Because this is an open-book exam, simply searching for definitions may not be enough. Many questions will describe a cloud architecture or situation and ask you to select the most appropriate service, configuration, or design decision.
All material covered so far may be relevant. The following guide identifies the major concepts and skills you should focus on when preparing for the exam.

**Note:** Generative AI tools may not be used during the exam.

## 1. Cloud Computing Fundamentals

Understand the major characteristics and benefits of cloud computing.

You should be able to:

- Explain how cloud computing differs from simply running a few physical servers on-premises.
- Describe major advantages of cloud computing.
- Explain **scalability** and **elasticity**.
- Distinguish between scalability and elasticity.
- Explain why virtualization is important in cloud computing.
- Identify important considerations when moving an application to the cloud.
- Explain why simply moving an application to a cloud VM does not necessarily mean the application was designed for the cloud.


---

## 2. Cloud Service Models

Understand the differences among:

- **Infrastructure as a Service (IaaS)**
- **Platform as a Service (PaaS)**
- **Serverless / Functions as a Service (FaaS)**
- **Software as a Service (SaaS)**

For each model, you should be able to:

- Identify what the cloud provider manages.
- Identify what the customer manages.
- Select the most appropriate service model for a given scenario.

---

## 3. Compute Engine, Cloud Shell, and App Engine

### Google Cloud Projects, Regions, and Zones

You should understand:

- The purpose of a **Google Cloud project**.
- What a Google Cloud **region** is.
- What a Google Cloud **zone** is.
- That Google Cloud resources may have global, regional, or zonal scope.

### Google Cloud Console and Cloud Shell

Understand:

- The difference between the **Google Cloud Console** and **Cloud Shell**.
- Why Cloud Shell can be useful for managing cloud resources.
- The purpose of the `gcloud` command-line tool.

Given command syntax or a command reference, you should be able to identify commands that:

- Set the active Google Cloud project.
- Set the default Compute Engine region.
- Set the default Compute Engine zone.
- Create a Compute Engine VM.
- SSH into a Compute Engine VM.

You do **not** need to memorize every command flag exactly, but you should understand what the commands are doing.
### Compute Engine

Understand:

- What a Compute Engine VM is.
- What information is needed when creating a VM.
- The difference between an **internal IP address** and an **external IP address**.
- What must be configured for an Internet user to access a web server running on a VM.
- what are the commonly used network ports

### VPC Firewall vs. Guest OS Firewall

Understand that these are separate security layers:

- **Google Cloud VPC firewall**
- Firewall inside the VM, such as `ufw`

A connection can fail even if one firewall allows the traffic when the other firewall blocks it.

Also understand why we used the **serial console** when SSH access to a VM was accidentally blocked.

### App Engine

Understand:

- What App Engine is.
- The general process for deploying an application to App Engine.
- What `gcloud app deploy` does.
- Why a developer might choose App Engine instead of manually managing a Compute Engine VM.

---

## 4. Designing Cloud Applications

Cloud applications should be designed to take advantage of cloud capabilities rather than simply moving an existing application to a VM.

You should understand:

- Why applications should be designed to tolerate failures.
- What a **single point of failure** is.
- The difference between **scaling up** and **scaling out**.
- What an **instance template** is.
- What a **Managed Instance Group (MIG)** is.
- What an **autoscaler** does.
- How autoscaling can increase or decrease the number of VM instances as demand changes.

### Scaling

> **Scale up (vertical scaling)** = give one machine more resources.

> **Scale out (horizontal scaling)** = add more machines.

### Managed Instance Groups

An **instance template** defines how VM instances should be configured.

A **Managed Instance Group** manages a group of VM instances created from an instance template.

An **autoscaler** can change the size of the managed instance group based on demand.

---

## 5. VPC Networking and Firewall Rules

You should be able to apply networking concepts to a simple Google Cloud architecture or network diagram.

### VPCs and Subnets

Understand:

- What a **Virtual Private Cloud (VPC)** is.
- A Google Cloud VPC is **global**.
- A Google Cloud subnet is **regional**.
- The purpose of a subnet.
- The difference between **auto mode** and **custom mode** VPC networks.
- How do the resources in different subnets of the same VPC to communicate?

### Internal and External IP Addresses

Understand:

- **Internal IP addresses** are used for private communication within the cloud network.
- **External IP addresses** allow communication with resources outside the private cloud network, including the Internet.

### CIDR

Understand:

- What CIDR notation represents.
- The meaning of prefixes such as `/16` and `/24`.

### Routes and Firewall Rules

Understand the difference:

> **Route = where traffic goes**  
> **Firewall = whether traffic is allowed**

You should understand:

- The purpose of a route.
- The purpose of a firewall rule.
- The difference between **ingress** and **egress** traffic.
- What `0.0.0.0/0` means in an IPv4 firewall rule.
- How protocol and port numbers are used in firewall rules.
- The purpose of **network tags** when targeting firewall rules.

Be prepared to recognize appropriate firewall configurations for:

- SSH
- HTTP
- HTTPS

For example, if a public website needs to accept HTTP requests from Internet users, think about:

- Direction of traffic
- Source
- Protocol
- Port
- Which VMs should receive the traffic

---

## 6. Connecting Cloud Networks

You should understand when and why to use the following Google Cloud networking solutions:

- **Shared VPC**
- **VPC Network Peering**
- **Cloud VPN**
- **Dedicated Interconnect**
- **Partner Interconnect**

### Shared VPC

Use Shared VPC when:

> Multiple Google Cloud projects should use **one centrally managed VPC network**.

Remember:

> **Shared VPC = one network, multiple projects**

### VPC Network Peering

Use VPC Network Peering when:

> Two separate VPC networks need to communicate privately while remaining independently managed.

Remember:

> **VPC Peering = separate networks connected privately**

### Cloud VPN

Cloud VPN is appropriate when:

- An on-premises network needs to connect to Google Cloud.
- The connection should be encrypted.
- Traffic can travel over the public Internet.

### Cloud Interconnect

Use Interconnect when an organization requires higher-capacity private connectivity between an on-premises network and Google Cloud.

Understand the basic difference between:

- **Dedicated Interconnect** — direct physical connectivity to Google
- **Partner Interconnect** — connectivity through a supported service provider

---

## 7. Cloud Load Balancing, MIGs, and Autoscaling

Understand why cloud applications use load balancing and how load balancing works together with managed instance groups and autoscaling.

### Why Load Balance?

A load balancer:

- Provides a common frontend for clients.
- Distributes incoming traffic across backend resources.
- Helps improve availability.
- Avoids sending new traffic to unhealthy backends.

### Application vs. Network Load Balancing

Understand the basic distinction:

- **Application Load Balancer** — Layer 7, primarily HTTP/HTTPS traffic
- **Network Load Balancer** — Layer 4, primarily TCP/UDP and other network traffic

You do not need to memorize the complete OSI model, but you should understand why an HTTP/HTTPS web application is normally associated with an **Application Load Balancer**.

### Frontends and Backends

Understand:

- **Frontend** = where clients connect
- **Backend** = resources that actually process requests
- **Backend service** = connects the load balancer to its backend resources

### Health Checks

A health check determines whether a backend is able to serve traffic.

Understand that:

- Healthy backends can receive new traffic.
- An unhealthy backend should stop receiving new traffic.
- A health check detects backend health.
- A health check does **not** itself create or remove VM instances.

### Load Balancing and Autoscaling

Understand the relationship among:

- **Load Balancer**
- **Health Check**
- **Managed Instance Group**
- **Instance Template**
- **Autoscaler**

Remember:

> **Load balancing handles traffic.**  
> **Autoscaling handles capacity.**

For example:

- The **load balancer** distributes requests among healthy backend instances.
- The **health check** determines whether a backend can serve traffic.
- The **MIG** manages a group of consistently configured VM instances.
- The **autoscaler** increases or decreases the number of VM instances as demand changes.

### External vs. Internal Load Balancing

Understand:

- An **External Application Load Balancer** can provide a frontend for Internet users.
- An **Internal Application Load Balancer** can provide a private frontend for clients inside the cloud network.

You should be able to select the appropriate type based on whether the application should be publicly or privately accessible.
