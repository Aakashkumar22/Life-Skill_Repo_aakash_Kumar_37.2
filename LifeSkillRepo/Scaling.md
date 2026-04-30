# Scaling in System Design

Scaling is one of the most important concepts in system design and software development. As an application grows, the number of users, requests, and data also increases.

If the system is not designed to handle this growth, it can become slow, crash frequently, or stop working completely.

Scaling is the process of increasing the system’s capacity so it can handle more traffic and workload smoothly.
<p align="center">
  <img src="https://github.com/user-attachments/assets/3fc68461-5467-4a64-8f32-4ccfa8badd15" width="500" height="300" />
</p>






---

# Why We Are Learning Scalability

In the previous article, we designed an e-commerce application using Clean Architecture and identified performance limitations regarding concurrent requests.

### Problem
  Increased traffic
 <p align="center">
  <img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/a3eaedc3-3c06-4af0-88cd-ff36431e71bb" />
  </p>

* Need to handle more requests per second

### Current limitation
* System handles only ~2K concurrent requests per second

As the business grows, the system must support higher load with acceptable latency.

---

# Problem and Solution Overview

To handle scaling challenges, we consider:

* Vertical Scaling
* Horizontal Scaling
  <p align="center">
  <img width="300" height="168" alt="image" src="https://github.com/user-attachments/assets/aec27a67-cb8a-420a-bfe1-8061d40b301d" />
  </p>


  
  


---

# Non-Functional Requirements (NFR)

Scalability is one of the most important non-functional requirements and must be considered from day one.Scalability is simply measured by the number of requests an application can handle successfully. It can be measured by the number of requests and it can effectively support simultaneously. Once the application can no longer handle any more simultaneous requests, it has reached its scalability limit. When your business to grow, in order to prevent downtime, and reduce latency, you must scale your resources accordingly. You can scale these resources through a combination of the network bandwidth, CPU and physical memory requirements, and hard disk adjustments.

Key NFRs:
* Scalability
* Performance
* Availability
* Reliability

---

# What is Scalability?

Scalability is the ability of a system to handle increased load while maintaining performance and responsiveness.

A system is scalable if it can:
* Handle more users
* Process more requests
* Manage higher data volumes

Once a system reaches its limit, performance degradation occurs.

---

# Why Scalability is Important

Without scalability:
* Slow response times
* System crashes
* Downtime
* Poor user experience

Scaling ensures the system grows with business demand.

---

# Types of Scalability

There are two main types:

* Vertical Scaling (Scale Up)
* Horizontal Scaling (Scale Out)
<p align="center">
  <img src="https://github.com/user-attachments/assets/92dc9094-fd52-42ea-a09e-abdeb81f9600" width="631" height="415" />
</p>



---

# Vertical Scaling (Scale Up)

Vertical scaling means increasing resources of a single machine.
<p align="center">
  <img src="https://github.com/user-attachments/assets/786f0360-837f-4f74-939c-f3b467c38db7" width="500" height="300" />
</p>
Vertical Scaling is offers to increasing the resources of a single server or node, such as increasing the CPU, memory, or storage capacity. This approach is also known as scaling up, and it is commonly used for database systems and other types of software that require high performance.

Vertical scaling is basically makes the nodes stronger. If you have 1 server, make the server stronger with adding more hardware. Make optimization the hardware that will allow you to handle more requests. Vertical scaling keeps your existing infrastructure but adding more computing power. Your existing code doesn’t need to change — you simply need to run the same code on machines with better specs. Vertical scaling means adding more resources to a single node and adding additional CPU, RAM, and DISK to cope with an increasing workload.





### How it works
* Add CPU
* Add RAM
* Add storage

### Advantages
* Simple architecture
* Easy to implement
* No code changes required

### Disadvantages
* Hardware limits
* Expensive at scale
* Single point of failure

### Key idea
Make one machine stronger.

---

# Horizontal Scaling (Scale Out)

Horizontal scaling means adding more machines to distribute the load.
<p align="center">
  <img src="https://github.com/user-attachments/assets/0054fb25-c413-4c2c-81b5-968685b14dad" width="500" height="300" />
</p>
Horizontal Scaling is offers to adding more servers or nodes to the system in order to increase its capacity to handle more traffic. This approach is also known as scaling out, and it is commonly used for web applications and distributed systems.

Horizontal scaling basically means splitting the load between different servers. Horizontal scaling simply adds more instances of machines without changing to existing specifications. By scaling out, you can share the processing power and load balancing across multiple machines.

Horizontal scaling means adding more machines to the resource pool, rather than simply adding resources by scaling vertically. Scaling horizontally gives you scalability but also reliability because you will have more redundancy and mostly its the preferred way to scale in distributed architectures.





### How it works
* Add multiple servers
* Distribute traffic using load balancer

### Advantages
* Highly scalable
* Fault tolerant
* Better performance distribution

### Disadvantages
* Complex system design
* Requires load balancing
* Data consistency challenges



 # References for Scaling in High-Level Design (HLD)

## 📘 Articles & Blogs

* Scalability Resources Collection  
  https://awesome-architecture.com/scaling/  

* System Design of YouTube (Scalability Example)  
  https://www.geeksforgeeks.org/system-design/system-design-of-youtube-a-complete-architecture/  

* YouTube System Design & Scalability Guide  
  https://intervu.dev/blog/youtube-system-design/  

* YouTube Scalability Techniques (Real-world case study)  
  https://newsletter.systemdesign.one/p/youtube-scalability  

---

## 📚 Books (Highly Recommended)

* Designing Data-Intensive Applications — Martin Kleppmann  
* System Design Interview Vol 1 & 2 — Alex Xu  
* Understanding Distributed Systems — Roberto Vitillo  
* Database Internals — Alex Petrov  
* Architecting for Scale — Lee Atchison  

---

## 🎥 YouTube Learning

### System Design Scalability Guide

::contentReference[oaicite:0]{index=0}


---

## 📺 Best YouTube Channels for HLD & Scaling

* ByteByteGo (visual system design & scalability)
* Gaurav Sen (strong fundamentals)
* Exponent (interview-focused system design)
* Hussein Nasser (deep backend & scaling concepts)

---

* https://www.nginx.com/resources/glossary/load-balancing/
* https://martinfowler.com/articles/microservices.html
