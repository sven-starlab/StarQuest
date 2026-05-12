# STARQUEST - Onboarding 
This module is designed to take you from conceptual theory to hands-on mastery. You will progress through three distinct stages: 
**Interactive Learning & Theory** → **Troubleshooting** → **Building**.

# Topic 1: Containerization Fundamentals (Docker & K8s)

## I. Interactive Learning & Theory
*Goal: Build your foundation using a hands-on approach.*

- **Theory:**
    Watch the [Video Playlist](https://www.youtube.com/watch?v=1fL54Q-wa54&list=PLe0BjvzMsG7T2nTzWoRGIODG43cAvne27). This covers the core concepts of Docker images, Kubernetes pods, and how OpenShift manages enterprise clusters.
    
- **Sandbox:**
    Navigate to Killercoda and complete them all. Much like using W3Schools for coding, you will use these interactive terminals to practice commands in real-time.
    - [Killercoda for Docker](https://killercoda.com/docker)
    - [Killercoda for Kubernetes](https://killercoda.com/kubernetes)
    
- **Checkpoint (Reflection 1):**
    After completing the labs, submit a brief summary of some important commands or actions you learned. Please specify if you preferred using the Docker Desktop / Lens GUI or the PowerShell / CLI method for your tasks.
    - *(Optional)* Since Killercoda is terminal-only (CLI), how did your experience there compare to using the GUI tools on your local machine?

---

## II. Troubleshooting
*Goal: Develop your troubleshooting skills by fixing a broken system.*

### Part A
- **The Scenario:**
    You have been handed a pre-existing project. However, the system is failing: the container won't build, and the deployment on the cluster is unreachable.
    
- **Your Task:**
    **[Insert links to Broken Dockerfile and Broken K8s YAML here]**. You must investigate both files to identify and resolve the intentional configuration errors. These may include:
    - **Build Errors:** Syntax issues or broken commands within the **Dockerfile**.
    - **Deployment Errors:** Image name typos, port mismatches, or resource errors within the **Kubernetes YAML**.

- **The Objective:**
    Using your preferred workflow, either **GUI (Docker Desktop / Lens)** or **CLI (PowerShell / kubectl),** successfully build the image and return the application to a healthy and accessible state on the cluster.
    
- **Checkpoint (Reflection 2A):**
    Document the specific errors you discovered in both the Docker and Kubernetes configurations. Explain the logic and the specific tools you used to track down the root cause (e.g., "I used `docker build` logs to find the syntax error" or "I checked the Events tab in Lens to see the Port mismatch").

### Part B
- **Your Task:**
    Navigate to [Killercoda Kubernetes Troubleshooting Challenge](https://killercoda.com/touching/course/scenarios) and complete them all.
    
- **Checkpoint (Reflection 2B):**
    Document the specific errors you discovered. Explain the logic you used to track down the root cause of each failure.

---

## III. Building
*Goal: Apply your knowledge to build a full-stack solution from scratch.*

- **The Strategy:**
    1.  **Docker First:** Build and run each service individually as a Docker container to ensure they are functional.
    2.  **Orchestration:** Once the containers run locally, deploy the full stack into a Kubernetes environment.

- **The Tools:**
    You may choose the method that best fits your workflow. You can use **Minikube** (CLI) or **Lens/Docker Desktop** (GUI) to manage your cluster.
    
- **The Assignment:**
    Using the provided **Architecture Map**, you are required to build and deploy a multi-tier microservice.
    
    **[Insert Architecture Map here]**
    
- **The Requirements:**
    - There is no step-by-step guide. You must research and implement the networking required for services to communicate.
    - **OpenShift (Optional):** If you have access to the dev cluster, attempt to expose your "Gateway" service using an **OpenShift Route**.

- **Final Reflection:**
    A brief retrospective on your process. Why did you choose your specific toolset (GUI vs. CLI), and how did the "Docker-First" step help you when you moved to Kubernetes?
