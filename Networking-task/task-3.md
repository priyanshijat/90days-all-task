# 🚀 What is an EC2 Instance & How to Launch it on AWS ❓
*#90daysofdevops – Week 1 Task 3: Launching an EC2 Instance*

---

## 💡 What is an EC2 Instance?

*EC2 (Elastic Compute Cloud)* is a virtual server running in the AWS cloud.  
Instead of owning physical hardware, AWS allows us to rent virtual machines on-demand.  
We only pay for what we use, and can *launch, stop, start, and terminate instances* within seconds.

---

## 🏠 Real-life Analogy:

Imagine *renting an apartment (EC2 instance)* in a *high-rise building (AWS Cloud)*.  
You can choose the *size, location, and features* (CPU, RAM, OS, etc.), and you *only pay while you use it*.

---

## 📌 Common Use Cases:

 ✅ Hosting web applications  
 ✅ Running backend services  
 ✅ Testing and development environments  
 ✅ Data processing  

---

## 💡 How to Launch an EC2 Instance on AWS

### 🔹 Step 1: Log in to AWS Console  
👉 [Go to AWS Console](https://lnkd.in/dzvGEhGy)

### 🔹 Step 2: Navigate to EC2 Service  
- Search for *"EC2"* in the AWS search bar  
- Click on *EC2* under Services  

### 🔹 Step 3: Click on “Launch Instance”  
- Go to the *Instances* section on the left panel  
- Click *Launch Instance*

### 🔹 Step 4: Configure Instance Details

- *Name & Tags*  
  Give your instance a recognizable name

- *Application & OS Image (AMI)*  
  Choose from options like *Amazon Linux 2, **Ubuntu, or **Windows*

- *Instance Type*  
  Select *t2.micro* (Free Tier eligible)

### 🔹 Step 5: Configure Key Pair (SSH Access)  
- Create a *new key pair* (if first time)  
- **Download the .pem file** — keep it safe for SSH access

### 🔹 Step 6: Configure Network Settings  
- Use default *VPC* and *subnet*  
- Allow *SSH (port 22)* for Linux or *RDP (port 3389)* for Windows  

### 🔹 Step 7: Add Storage (Optional)  
- Default is *8GB for Linux, **30GB for Windows*  
- Increase size based on your needs

### 🔹 Step 8: Review & Launch  
- Review all your settings  
- Click *Launch Instance*

### 🔹 Step 9: Connect to Your Instance  
- Go to *Instances*, select your instance  
- Click *Connect* → choose *EC2 Instance Connect* or *SSH*

#### 🖥 For SSH:
```bash
ssh -i "your-key.pem" ec2-user@your-public-ip