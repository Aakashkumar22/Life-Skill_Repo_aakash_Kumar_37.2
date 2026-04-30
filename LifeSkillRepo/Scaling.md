# Scaling in System Design

Scaling is one of the most important concepts in system design and software development. As an application grows, the number of users, requests, and data also increases.

If the system is not designed to handle this growth, it can become slow, crash frequently, or stop working completely.

Scaling is the process of increasing the system’s capacity so it can handle more traffic and workload smoothly.





---

# Why We Are Learning Scalability

In the previous article, we designed an e-commerce application using Clean Architecture and identified performance limitations regarding concurrent requests.

### Problem
* Increased traffic
* Need to handle more requests per second

### Current limitation
* System handles only ~2K concurrent requests per second

As the business grows, the system must support higher load with acceptable latency.

---

# Problem and Solution Overview

To handle scaling challenges, we consider:

* Vertical Scaling
* Horizontal Scaling
* Load Balancing

---

# Non-Functional Requirements (NFR)

Scalability is one of the most important non-functional requirements and must be considered from day one.

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

---

# Vertical Scaling (Scale Up)

Vertical scaling means increasing resources of a single machine.

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




* https://aws.amazon.com/architecture/
* https://www.nginx.com/resources/glossary/load-balancing/
* https://martinfowler.com/articles/microservices.html
