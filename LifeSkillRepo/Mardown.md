# Load Balancer Overview

A load balancer is a device or software acting as a traffic cop, often described as a reverse proxy, that sits in front of servers to distribute incoming network traffic. It improves application availability, performance, and reliability.

It ensures no single server is overloaded, prevents downtime, and improves scalability.

---

# Load Balancer Architecture Diagram

![Load Balancer Architecture](https://upload.wikimedia.org/wikipedia/commons/6/6b/Load_balancer.svg)

---

# Types of Load Balancers Based on OSI Model

## Network Load Balancer (Layer 4)

![Layer 4 Load Balancer](https://upload.wikimedia.org/wikipedia/commons/1/1e/OSI_model_L4_load_balancing.png)

Layer 4 load balancers work at the transport layer and route traffic based on:
* IP address
* Port number

### How it works
1. Receives request
2. Reads IP and port
3. Selects server
4. Forwards request

---

## Application Load Balancer (Layer 7)

![Layer 7 Load Balancer](https://upload.wikimedia.org/wikipedia/commons/3/3c/OSI_model_L7_load_balancing.png)

Layer 7 load balancers inspect application-level data like:
* URLs
* Cookies
* HTTP headers

### How it works
1. Reads HTTP request
2. Analyzes content
3. Routes based on rules
4. Sends request to best server

---

# Load Balancing Algorithms

## 1. Round Robin

![Round Robin](https://upload.wikimedia.org/wikipedia/commons/4/4e/Round-robin_load_balancing.png)

### Flow
Client requests → Server A → Server B → Server C → repeat cycle

---

## 2. Weighted Round Robin

![Weighted Round Robin](https://upload.wikimedia.org/wikipedia/commons/0/09/Weighted_round_robin_load_balancing.png)

Servers with higher weight get more traffic.

---

## 3. IP Hash

![IP Hash Load Balancing](https://upload.wikimedia.org/wikipedia/commons/2/2b/Load_balancing_IP_hash.svg)

Same client IP always goes to same server.

---

## 4. Least Connection

![Least Connection](https://upload.wikimedia.org/wikipedia/commons/5/5e/Least_connections_load_balancing.png)

New requests go to server with least active connections.

---

## 5. Least Response Time

![Least Response Time](https://upload.wikimedia.org/wikipedia/commons/9/9f/Response_time_load_balancing.png)

Routes traffic to fastest responding server.

---

# Advantages of Load Balancer

* Improves availability
* Prevents server overload
* Increases scalability
* Ensures fault tolerance

---

# Disadvantages

* Adds extra infrastructure layer
* Can become bottleneck if misconfigured
* Requires monitoring and setup

---

# References

* https://aws.amazon.com/what-is/load-balancing/
* https://www.nginx.com/resources/glossary/load-balancing/
* https://www.cloudflare.com/learning/performance/what-is-load-balancing/
* https://www.f5.com/services/resources/glossary/load-balancer
