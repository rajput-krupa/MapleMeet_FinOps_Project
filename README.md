# ☁️ Maple Meet – AWS Cloud Infrastructure & FinOps Optimization 💸

Welcome to my hands-on AWS + FinOps project where I acted as a **Cloud FinOps Consultant** for a fictional Canadian startup – **Maple Meet**. The project simulates a real-world scenario where I architected, deployed, and optimized cloud infrastructure while reducing costs and enhancing financial visibility.

---

## 🧩 About the Project

**Maple Meet** is a growing virtual event platform that recently migrated to AWS. Their monthly cloud bills were increasing without clear visibility. My role was to:

🔹 Architect scalable AWS infrastructure  
🔹 Implement financial governance (FinOps)  
🔹 Identify waste & optimize services (EC2, S3, EBS)  
🔹 Visualize the changes using diagrams, dashboards, and reports

---

## 🛠️ AWS Services Used

| Category         | Services Used                         |
|------------------|----------------------------------------|
| **Compute**      | EC2, EBS                              |
| **Storage**      | S3 (with lifecycle & classes)         |
| **Security**     | IAM, Key Pairs, Security Groups       |
| **Monitoring**   | CloudWatch, Cost Explorer, Budgets    |
| **Networking**   | Elastic IPs, VPC (basic setup)        |
| **Optional**     | S3 Static Website Hosting             |



## 🧠 What I Did – Hands-On Breakdown

### 1️⃣ IAM – Identity & Access Management  
- Created users, groups, and roles using best practices (least privilege)  
- Implemented MFA and console-only access for admins  
- Logged all steps with reasoning and diagrams

### 2️⃣ EC2 – Compute Resource Setup  
- Launched Linux EC2 for hosting backend service  
- Connected via SSH using PuTTY and AWS CLI  
- Attached and mounted EBS volumes  
- Hosted basic website using EC2 User Data script

### 3️⃣ EC2 FinOps Optimization 💸  
- Right-sized instances (t2.micro → t3.nano for dev)
- Scheduled non-prod instance shutdown during off hours  
- Tagged all EC2 resources by environment (dev/prod)  
- Monitored cost changes using Cost Explorer

### 4️⃣ S3 – Storage for Static Assets  
- Created versioned buckets with defined folder structures  
- Enabled S3 static website hosting (optional feature)  
- Applied permissions via bucket policies and IAM roles

### 5️⃣ S3 FinOps Optimization 💸  
- Applied lifecycle rules to move old data to Infrequent Access & Glacier  
- Enabled logging and object versioning  
- Deleted unnecessary objects using CLI script

### 6️⃣ EBS Optimization 💸  
- Switched from `gp2` to `gp3`  
- Identified and deleted unused volumes  
- Set automated snapshot rules using AWS Backup

### 7️⃣ Cost Monitoring & Dashboards 📊  
- Created AWS Budgets and alerts (email + console)  
- Used CloudWatch to track usage metrics  
- Created a Cost Explorer dashboard (before vs after)

---

## 💰 Key Savings Snapshot

| Service | Strategy Applied                        | Monthly Savings |
|---------|------------------------------------------|-----------------|
| EC2     | Right-sizing + Scheduling                | ~$20/month      |
| S3      | Lifecycle policies + IA/Glacier storage  | ~$8/month       |
| EBS     | gp3 conversion + cleanup                 | ~$6/month       |
| **Total** |                                          | **~$34/month**  |

> Simulated on free-tier with extrapolated cost estimates

---

## 📊 Visuals & Diagrams

- ✅ **[initial-setup.drawio](architecture/initial-setup.drawio)** – Original AWS setup
- ✅ **[optimized-setup.drawio](architecture/optimized-setup.drawio)** – Cost-optimized architecture
- ✅ Screenshots of EC2 Console, Cost Explorer, Lifecycle Policies

---

## 🔍 Key FinOps Concepts Applied

- **Visibility**: Tracked spend by tagging resources (env, project)  
- **Optimization**: Identified unused & over-provisioned resources  
- **Accountability**: Created dashboards & documented every decision  
- **Automation**: Lifecycle rules, snapshot policies, auto-shutdown

---

## 👨‍💻 Skills Demonstrated

- ✅ AWS Infrastructure Design
- ✅ FinOps Principles (Cloud Cost Optimization)
- ✅ EC2, S3, IAM, CloudWatch, Budgets
- ✅ Hands-on monitoring, reporting, automation
- ✅ Documentation, diagramming, client-like reporting

---

## 🎯 Why This Project?

> “Cloud engineers need to understand cost. FinOps makes you not just a user of AWS, but a **responsible architect**.”

This project helped me:
- Build real FinOps skills (not theory!)
- Combine cloud engineering + financial accountability
- Communicate technical setups to non-technical stakeholders
