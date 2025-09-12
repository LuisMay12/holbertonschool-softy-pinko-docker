# holbertonschool-softy-pinko-docker

# Docker Project - Reverse Proxy, Load Balancer, and Application Infrastructure

## 📖 Context

Docker is a platform that allows you to **containerize your applications**, meaning that you can package them into portable, self-contained environments which can run anywhere.  

This means you can quickly move your application from one environment to another — such as from your local computer to a server — without worrying about dependencies or configuration issues.

Docker achieves this by using **containers**, which are isolated environments that contain everything an application needs to run (libraries, dependencies, configurations). Containers are lightweight and can be started/stopped quickly, making them ideal for modern software development and deployment.

With Docker, you can also quickly **scale your application** by running multiple containers of the same application on different hosts (or the same host), and manage them using **Docker Compose** or orchestration tools.

---

## 🏗️ High-level Design

Ths¿is create an infrastructure for an application that utilizes:

- A **reverse proxy**  
- A **load balancer**  
- **Two application servers (API)**  
- **One front-end server**

### 🔹 Workflow

1. **Single entry point**:  
   The proxy server acts as the entry point for all client requests.  

2. **Reverse Proxy Role**:  
   - Routes traffic either to the **front-end static-content server** or the **API servers**.  
   - The client never directly communicates with backend servers.  

3. **Load Balancer Role**:  
   - Balances requests between the **two API servers**.  
   - Uses the **Round Robin algorithm** to evenly distribute requests.  

---

## ⚖️ What is Round Robin Load Balancing?

**Round Robin** is a simple method to distribute traffic across multiple servers.  
Each request is assigned to a server in rotation.  

Example with 3 servers (A, B, C):  
- 1st request → A  
- 2nd request → B  
- 3rd request → C  
- 4th request → A  
- and so on...  

This ensures fairness and avoids overwhelming a single server.  
⚠️ Note: While effective for learning purposes, it may not be suitable for workloads with uneven resource requirements.

---

## 🛠️ What You Need Before Starting

1. **Install Docker Desktop**  
   👉 [Download Docker](https://www.docker.com/)  

   - [Windows Installation Guide](https://docs.docker.com/desktop/install/windows/)  
   - [Mac Installation Guide](https://docs.docker.com/desktop/install/mac/)  
   - [Linux Installation Guide](https://docs.docker.com/desktop/install/linux/)  
   - Chromebook: Docker Engine may work, but Docker Desktop is not supported. Prefer Windows, Mac, Linux, or a campus machine.

2. **Familiarize Yourself with Docker**  
   - [Docker Tutorial](https://docs.docker.com/get-started/)  
   - [Docker Cheatsheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)  

3. **Understand Reverse Proxies**  
   - [Proxy vs Reverse Proxy (Examples)](https://www.imperva.com/learn/application-security/reverse-proxy/)  
   - [What is a Reverse Proxy? (Video, stop at 06:25)](https://www.youtube.com/watch?v=IywVQV54qfo)  

---

## 📚 Useful Resources

- [Docker Documentation](https://docs.docker.com/)  
- [Docker Compose Overview](https://docs.docker.com/compose/)  
- [Reverse Proxy Explained](https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/)  

