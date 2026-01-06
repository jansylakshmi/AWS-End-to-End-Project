a# 🚀 End-to-End AWS Project

## Auto-Scalable Application with Monitoring, Storage & Notifications

This project demonstrates a **beginner-to-intermediate, production-style AWS architecture** using managed services to deploy, scale, monitor, and secure an application.

It is **GitHub-ready**, **resume-friendly**, and ideal for **DevOps / Cloud Engineer roles**.

---

## 🧩 Services Used

* **Elastic Beanstalk** – Application deployment & management
* **EC2 (Elastic Compute Cloud)** – Compute instances
* **Auto Scaling** – Automatic scaling based on load
* **S3 (Simple Storage Service)** – File & object storage
* **CloudWatch** – Monitoring & alarms
* **SNS (Simple Notification Service)** – Email alerts
* **IAM** – Secure access management

---

## 🎯 Project Objective

Deploy a web application using **Elastic Beanstalk**, enable **automatic EC2 scaling**, store application data in **S3**, monitor system performance using **CloudWatch**, and send **email notifications using SNS** when performance thresholds are breached.

---

## 🏗️ Architecture Flow (Simple)

```
User
  ↓
Elastic Beanstalk Environment
  ↓
EC2 Instances (Auto Scaling Group)
  ↓
CloudWatch Monitoring
  ↓
SNS Notifications
  ↓
S3 Storage
```

---

## ⚙️ Step-by-Step Implementation

### 🔹 Step 1: Create S3 Bucket for Storage

**Purpose:** Store application files, assets, or logs.

1. Go to **AWS Console → S3**
2. Click **Create bucket**
3. Bucket name: `app-storage-demo`
4. Keep default settings
5. Create the bucket
6. Upload a sample file (text/image)

Optional CLI verification:

```bash
aws s3 ls
aws s3 ls s3://app-storage-demo
```

---

### 🔹 Step 2: Create SNS Topic for Alerts

**Purpose:** Receive email notifications when alarms are triggered.

1. Go to **SNS → Topics → Create topic**
2. Type: **Standard**
3. Name: `app-alerts`
4. Create a subscription

   * Protocol: **Email**
   * Endpoint: *your email address*
5. Confirm the subscription from email

---

### 🔹 Step 3: Deploy Application Using Elastic Beanstalk

**Purpose:** Deploy and manage the application with auto-scaling.

1. Go to **Elastic Beanstalk**
2. Click **Create application**
3. Application name: `sample-app`
4. Environment type: **Web server environment**
5. Platform: **Python / Node.js**
6. Application code: **Sample application**
7. Instance type: `t2.micro`
8. Create environment

Elastic Beanstalk automatically provisions:

* EC2 instances
* Auto Scaling Group
* Load balancer (if enabled)
* CloudWatch monitoring

Wait until the environment status becomes **Green (Healthy)** ✅

---

### 🔹 Step 4: Verify EC2 & Auto Scaling

**Purpose:** Ensure scaling is correctly configured.

1. Go to **EC2 → Instances**

   * Verify instances launched by Elastic Beanstalk
2. Go to **EC2 → Auto Scaling Groups**

   * Minimum capacity: `1`
   * Desired capacity: `2`
   * Maximum capacity: `3`

---

### 🔹 Step 5: Configure CloudWatch Alarm

**Purpose:** Monitor CPU usage and trigger alerts.

1. Go to **CloudWatch → Alarms → Create alarm**
2. Select metric: **EC2 → CPUUtilization**
3. Condition: **CPU > 70%**
4. Alarm action: **Send notification to SNS topic `app-alerts`**
5. Create the alarm

---

### 🔹 Step 6: Allow EC2 Secure Access to S3 (IAM Role)

**Purpose:** Enable EC2 to access S3 securely without access keys.

1. Go to **IAM → Roles → Create role**
2. Trusted entity: **EC2**
3. Attach policy: **AmazonS3ReadOnlyAccess**
4. Attach the role to Elastic Beanstalk EC2 instances

Verify access from EC2:

```bash
aws s3 ls
aws s3 ls s3://app-storage-demo
```

---

## 🔐 Security Best Practices

* IAM role-based access (no hardcoded credentials)
* CloudWatch monitoring for proactive alerting
* Auto Scaling to handle traffic spikes safely

---


  

    
