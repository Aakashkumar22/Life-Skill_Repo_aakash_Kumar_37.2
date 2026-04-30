# Load Balancer Overview

A load balancer is a device or software acting as a traffic cop, often described as a reverse proxy, that sits in front of servers to distribute incoming network traffic. It improves application availability, performance, and reliability.

It ensures no single server is overloaded, prevents downtime, and improves scalability.

---

# Load Balancer Architecture Diagram

 <img width="720" height="347" alt="image" src="https://github.com/user-attachments/assets/385d1c2c-a82f-4023-a90d-802dd97c63c1" />


---

# Types of Load Balancers Based on OSI Model
<img width="1100" height="258" alt="image" src="https://github.com/user-attachments/assets/07cd5213-b36c-411f-ab5d-010849f71655" />


## Network Load Balancer (Layer 4)
<img width="376" height="134" alt="image" src="https://github.com/user-attachments/assets/1b8cb98e-58e5-4808-b94e-3b85ced88d36" />



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

<img width="276" height="183" alt="image" src="https://github.com/user-attachments/assets/a25c2f5e-b061-47a1-8fa0-57647d3c7d21" />


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
<img width="720" height="449" alt="image" src="https://github.com/user-attachments/assets/43d88458-6c3a-42c7-a39f-a4bee0ad0b99" />


### Flow
Client requests → Server A → Server B → Server C → repeat cycle

---

## 2. Weighted Round Robin

<img width="720" height="478" alt="image" src="https://github.com/user-attachments/assets/37fc4f08-9d6b-4178-adda-c1bbc44c1359" />


Servers with higher weight get more traffic.

---

## 3. IP Hash

<img width="720" height="376" alt="image" src="https://github.com/user-attachments/assets/c8ef5114-97e1-4d69-a891-489f2d6ca368" />


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


* AWS Load Balancing Overview  
  https://aws.amazon.com/what-is/load-balancing/

* NGINX Load Balancing Guide  
  https://www.nginx.com/resources/glossary/load-balancing/

* Cloudflare Learning: Load Balancing  
  https://www.cloudflare.com/learning/performance/what-is-load-balancing/

* F5 Load Balancer Basics  
  https://www.f5.com/services/resources/glossary/load-balancer

* GeeksforGeeks - Load Balancer in System Design  
  https://www.geeksforgeeks.org/system-design/what-is-load-balancer-system-design/

* Microsoft Azure Load Balancer Documentation  
  https://learn.microsoft.com/en-us/azure/load-balancer/load-balancer-overview

* Google Cloud Load Balancing  
  https://cloud.google.com/load-balancing/docs/load-balancing-overview

* HAProxy Documentation  
  https://www.haproxy.org/#docs

* https://aws.amazon.com/what-is/load-balancing/
* https://www.nginx.com/resources/glossary/load-balancing/
* https://www.cloudflare.com/learning/performance/what-is-load-balancing/
* https://www.f5.com/services/resources/glossary/load-balancer
