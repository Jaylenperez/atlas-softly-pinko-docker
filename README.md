Docker is a platform for packaging applications into portable, self-contained containers that can run anywhere, ensuring consistent performance across different environments. These containers include all necessary libraries, dependencies, and configurations, making it easy to move applications from local development to production without compatibility issues. Docker containers are lightweight and can be quickly started or stopped, facilitating modern software development and deployment. Additionally, Docker supports scaling applications by running multiple instances across various hosts and managing them with tools like Docker Compose.

In this project, you will create an application infrastructure featuring a reverse proxy, load balancer, two API servers, and a front-end server.

High-level Design:
A single server acts as an entry point, functioning as both a reverse proxy and load balancer. It routes traffic either to the front-end static-content server or the API servers. For the front-end, the proxy forwards requests and returns the static content to the client. For the API, the proxy uses a Round Robin algorithm to distribute requests evenly between the two API servers, ensuring balanced load distribution. The responses are then sent back to the client through the proxy server.

Round Robin Load Balancing:
This method distributes incoming traffic sequentially across multiple servers, ensuring each server gets an equal share of requests. For example, with three servers (A, B, C), requests are assigned in a rotating manner: first to A, then B, then C, and the cycle repeats. This simple approach prevents any single server from becoming overloaded, though it might not be suitable for applications with uneven workload patterns. For the purposes of this project, it is an effective method for load balancing.






