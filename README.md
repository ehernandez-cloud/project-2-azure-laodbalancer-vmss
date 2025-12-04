# Project 2 — Azure Load Balancer + VM Scale Set + Autoscaling

This project demonstrates a highly available web application deployed on Azure using a **Virtual Machine Scale Set (VMSS)** behind a **Load Balancer (LB)**. The solution automatically scales based on CPU usage and distributes traffic evenly across instances.

---

## 📌 Architecture Overview


- **VNet + Subnet** for network isolation  
- **Public Load Balancer** with:
  - Frontend IP
  - Backend pool
  - Health probe
  - Load-balancing rules
- **VM Scale Set** (Linux)
  - Custom Script Extension installs web server
  - Autoscaling between 2–5 instances based on CPU
- **Scaling Rules**
  - Scale out: CPU > 60%
  - Scale in: CPU < 30%

---

## 🧩 What This Project Covers

- Creating a VNet + Subnet
- Deploying a Public Load Balancer
- Configuring:
  - Frontend IP
  - Health probe
  - Backend pool
  - Load balancing rule (port 80)
- Deploying a Linux VM Scale Set
- Adding a Custom Script Extension to install NGINX
- Scaling the VMSS to 2 instances
- Configuring Autoscale rules
- Testing the deployment from a web browser

---

## 🖼 Screenshots

### **1. Virtual Network & Subnet**
![Subnet Web](Screenshots/Subnet-Web.png)
![VNet LB](Screenshots/Vnet-LB.png)

---

### **2. Load Balancer Configuration**
**Frontend IP**
![LB Frontend IP](Screenshots/LB-IP-Frontend.png)

**Health Probe**
![LB Health Probe](Screenshots/Health-probel-LB.png)

**Load Balancing Rule**
![LB Rule](Screenshots/LB-Balancing-Rule.png)

---

### **3. VM Scale Set Deployment**
**Resource Group overview**
![RG LB ScaleSet](Screenshots/RG-LB-ScaleSet.png)

**VMSS deployed**
![VMSS Web](Screenshots/VMSS-Web.png)

**Custom Script Extension**
![Custom Script Linux](Screenshots/custom-script-linux.png)

---

### **4. Scaling**
**After setting instance count to 2**
![2 Instances](Screenshots/VMSS-2-Instances.png)

**Backend pool showing 2 healthy instances**
![Backend Pool](Screenshots/Backend-pool-2-instances.png)

---

### **5. Autoscaling Configuration**
![Autoscale Overview](Screenshots/VMSS-Autoscale-Overview.png)

---

### **6. Testing the Web Page**
![Browser Test](Screenshots/LB-Web-Browser.png)

---

## 🚀 Learnings & Takeaways

Through this project, I practiced:

- Designing scalable cloud architectures
- Configuring load balancing for high availability
- Using VM Scale Sets for elasticity
- Automating deployments using Custom Script Extensions
- Implementing autoscaling rules based on metrics
- Understanding backend pools & health probes
- Troubleshooting Azure networking components

This setup is commonly used in production environments for web applications, APIs, and stateless services.

---

## 📁 Repository Structure
