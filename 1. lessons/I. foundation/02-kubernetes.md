# Topic 2: Container Orchestration (Kubernetes)

## 🎯 The Purpose: Why Kubernetes?
If Docker is the "Container," Kubernetes (K8s) is the "Captain" of the ship. Running one container is easy, but managing hundreds across multiple servers is impossible to do manually. K8s automates the heavy lifting.

*   **The Problem:** Containers crash, traffic spikes, and servers fail. Manually restarting or scaling them 24/7 is not sustainable.
*   **The Solution:** Kubernetes acts as a self-healing brain. If a container dies, K8s restarts it. If traffic grows, K8s scales it. It ensures our apps stay online without human intervention.

---

## 👥 Internal Case Study: How We Use It
**(HELP ME REVIEW OR EDIT SOME QUESTIONS AND WHETHER ISIT RELEVANT)**

*Note: Interview the Cluster Admins or OCs to understand how Starlab manages its "fleet."*

1. Which clusters do we use (Minikube for local, OpenShift for Prod, or AWS/EKS)?
2. Do we have a "Gold Standard" for YAML files that everyone must follow?
3. What is the most common "Kubernetes Disaster" that has happened here because of a wrong configuration?

---

## 📅 Suggested Timeline (Total: ~2.5 Days)


| Phase | Time | Task | Goal (The Mission) |
| :--- | :--- | :--- | :--- |
| **Day 1** | 3 hrs | **Theory** | Learn the "Pods vs. Services" hierarchy. |
| | 4 hrs | **Sandbox** | Practice `kubectl` commands on Killercoda. |
| **Day 2** | 4 hrs | **Troubleshooting** | Fix "CrashLoopBackOff" and Networking errors. |
| | 4 hrs | **Building (Part A)** | Deploy your first multi-tier app into the cluster. |
| **Day 3** | 4 hrs | **Building (Part B)** | Expose your app to the outside world safely. |

---

## ✅ High-Level Learning Objectives
1.  **Master the Orchestrator's Brain:** Learn how to define a "Desired State" so the cluster manages container health automatically.
2.  **Speak the Language of YAML:** Learn to write deployment blueprints that are clean, reusable, and meet company standards.
3.  **Become a "Cluster Detective":** Use logs and events to diagnose why a pod is failing before it impacts the end user.

---

## 🛠️ Training Material

### I. Interactive Learning & Theory
**Goal:** Understand the K8s hierarchy (Nodes > Pods > Containers).

-   **Watch:** [Video Playlist](https://www.youtube.com/watch?v=1fL54Q-wa54&list=PLe0BjvzMsG7T2nTzWoRGIODG43cAvne27).
-   **Sandbox:** [Killercoda for Kubernetes](https://killercoda.com/kubernetes)
    -   *Focus:* "Kubernetes Basics" and "Deployment Strategies."

### II. Troubleshooting
**Goal:** Learn to stay calm and find the "smoking gun" when a deployment fails.

-   **The Scenario:** Your Docker image is perfect, but the Kubernetes deployment is stuck. The pods keep restarting.
-   **The Task:**
    Navigate to [Killercoda Kubernetes Troubleshooting Challenge](https://killercoda.com/touching/course/scenarios) and complete them all.errors.
-   **The Tool:** Use `kubectl describe pod` and `kubectl logs` to find out why the cluster is unhappy.

### III. Building
**Goal:** Turn your local Docker work into a live, scalable, and resilient cluster service.

-   **The Strategy:** Use **Minikube** or **Lens** to visualize your work. 
-   **The Assignment:** Deploy the microservice you built in Topic 1.
    -   Create a **Deployment** to run the pods.
    -   Create a **Service** to let the pods talk to each other.
-   **The Requirements:** Scale your application to 3 pods. Manually "kill" a pod and watch K8s bring it back to life.
-   **Final Reflection:** Why is it better to let K8s manage container restarts instead of doing it yourself via Docker?
