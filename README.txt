# Project 1: Manual Deployment of a Web Application on AWS EC2

This project demonstrates the foundational DevOps practice of manually deploying a simple web application. I have used a sample HTML application and deployed it on an **AWS EC2 instance**, configured with an **Nginx** web server to make it accessible to the world.

*(This repository is a fork of a sample application used for the sole purpose of demonstrating and documenting the deployment process).*

---

## 🎯 Project Objective

The primary goal was to gain hands-on experience with core cloud and server administration tasks. This manual process serves as a critical baseline, highlighting the challenges and pain points that automated CI/CD pipelines (covered in subsequent projects) are designed to solve.

---

## 🛠️ Technologies & Tools Used

*   **Cloud Provider:** AWS (Amazon Web Services)
*   **Compute Service:** EC2 (Elastic Compute Cloud) - Ubuntu Server 22.04
*   **Web Server:** Nginx
*   **Version Control:** Git & GitHub
*   **Networking:** AWS Security Groups, VPC, SSH
*   **Operating System:** Linux (Ubuntu)

---

## ⚙️ Deployment Workflow

The deployment process followed these steps:

1.  **Infrastructure Provisioning:**
    *   Launched a `t2.micro` EC2 instance on AWS within a default VPC.
    *   Created and attached a Security Group to the instance, configuring inbound rules to allow traffic on:
        *   **Port 22 (SSH)** for secure remote access from my IP.
        *   **Port 80 (HTTP)** for public web traffic.

2.  **Server Configuration:**
    *   Connected to the EC2 instance's command line using SSH and the `.pem` key.
    *   Updated the server's package manager (`sudo apt update`) and installed necessary software: Nginx web server (`sudo apt install nginx`) and Git (`sudo apt install git`).

3.  **Application Deployment:**
    *   Navigated to the Nginx web root directory (`/var/www/html`).
    *   Cloned this Git repository's application files into the directory using `sudo git clone .`.
    *   Verified that Nginx was active and serving the `index.html` file.

4.  **Verification:**
    *   Accessed the application by navigating to the EC2 instance's public IP address in a web browser to confirm a successful deployment.

---

## 📸 Verification Screenshots (Proof of Work)

The following screenshots serve as evidence of the successful deployment process.

**1. AWS EC2 Instance Provisioned**
...
![EC2 Dashboard](screenshots/ec2-dashboard.png)

**2. Nginx Service Status on Server**
...
![Nginx Status](screenshots/nginx-status.png)

**3. Final Deployed Website**
...
![Live Website](screenshots/live-website.png)

## 🧠 Key Learnings & Takeaways

*   **Practical Cloud Skills:** Gained tangible experience in provisioning, configuring, and accessing a virtual server on a major cloud platform.
*   **Importance of Network Security:** Understood the critical role of Security Groups in controlling network access. The application is inaccessible without the correct inbound rules.
*   **Linux Command-Line Proficiency:** Became more comfortable with essential Linux commands for package management (`apt`), file system navigation (`cd`, `ls`), and service administration (`systemctl`).

*   **The "Why" of Automation:** This entirely manual process is slow, requires direct server access, and is prone to human error. It clearly illustrates the immense value of automating this workflow with CI/CD pipelines, which is the logical next step.

