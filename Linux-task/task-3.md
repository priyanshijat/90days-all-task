# 📦 What Is a Volume?
In computing — especially in cloud and Linux systems — a volume refers to a storage unit that is mounted and used to store data, like a hard drive or partition.

## ✅ TASK: Mount a New AWS EBS Volume to /mnt/devops_data

### 🔧 Step 1: Create an EBS Volume
* Go to EC2 Dashboard → Elastic Block Store → Volumes → Create Volume.
* Set:

Size: e.g., 1 GiB

Availability Zone: must match your EC2 instance

Volume type: e.g., gp3
* Click Create Volume.

### 🔗 Step 2: Attach the Volume to Your EC2 Instance
* After creating the volume, select it and click Actions → Attach Volume.
* Choose your EC2 instance.
* It will be attached as a device (e.g., /dev/xvdf).
  
### Step 3: SSH into Your EC2 Instance
```bash
ssh -i your-key.pem ec2-user@<EC2_PUBLIC_IP>
```

### 🧱 Step 4: Create the Mount Directory
```bash
sudo mkdir -p /mnt/devops_data
```

### 🧹 Step 5: Check the New Disk and Format It
```bash
lsblk 
```
Format the volume (EXT4):
```bash
sudo mkfs.ext4 /dev/xvdf
```

### 📦 Step 6: Mount the Volume
```bash
sudo mount /dev/xvdf /mnt/devops_data
```

### 📊 Step 7: Verify the Mount
```bash
df -h
```
