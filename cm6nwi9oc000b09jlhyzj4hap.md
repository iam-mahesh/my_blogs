---
title: "Mastering AWS EC2 Security Groups & Essential Networking Commands 🚀"
datePublished: Sun Feb 02 2025 17:33:46 GMT+0000 (Coordinated Universal Time)
cuid: cm6nwi9oc000b09jlhyzj4hap
slug: mastering-aws-ec2-security-groups-essential-networking-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738516064309/3d2a4bac-41ee-4490-bc40-6566367d92f4.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1738517598006/ec422058-0fb3-4ed2-8d4a-32199b388bd0.png
tags: aws, devops, 90daysofdevops, 90daysofdevops-chanllenge, tws, ec2-instance

---

## **Introduction**

Whether you're launching your first AWS EC2 instance or troubleshooting network issues, mastering **Security Groups** and **networking commands** is crucial. In this guide, we’ll cover:

✅ How to **launch an AWS EC2 instance**  
✅ How to **configure Security Groups** for secure access  
✅ A **cheat sheet of essential networking commands**

## **🟢 Part 1: Launching an AWS EC2 Instance**

### **Step 1: Login to AWS & Navigate to EC2**

1. Go to [AWS Console](https://aws.amazon.com/) and sign in.
    
2. Search for **EC2** in the services menu.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738516536679/b93b22d1-9df1-45e7-ad4e-dcaa3498be4a.png align="center")

### **Step 2: Launch an EC2 Instance**

1. Click **Launch Instance**.
    
2. Choose an **Amazon Machine Image (AMI)** → Select Ubuntu **(Free Tier Eligible)**.
    
3. Choose an **Instance Type** → Select **t2.micro** (Free Tier).
    
4. Click **Next: Configure Security Group**.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738516696938/b1dd3561-ea73-47e0-8ea3-7b2500bacf3c.png align="center")

## **🟢 Part 2: Understanding Security Groups**

Security Groups in AWS act as **firewalls** that control **inbound & outbound traffic**.

### **Step 3: Configure Security Group Rules**

| **Rule** | **Protocol** | **Port** | **Source** | **Purpose** |
| --- | --- | --- | --- | --- |
| SSH | TCP | 22 | My IP | Secure remote access |
| HTTP | TCP | 80 | Anywhere | Allow web traffic |
| HTTPS | TCP | 443 | Anywhere | Secure web traffic |

1. Click **Review and Launch**.
    
2. **Download the Key Pair** (important for SSH access).
    
3. Click **Launch Instance**.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738517011984/c7efb372-8af5-44df-8c8a-2ee5f6e8707e.png align="center")

✅ **Done! Your EC2 instance is now live.**

## **🟢 Part 3: Essential Networking Commands Cheat Sheet**

### **1️⃣** `ping` - Check Network Connectivity

```plaintext
bashCopyEditping google.com
```

✅ Tests if a host is reachable.

### **2️⃣** `traceroute` / `tracert` - Trace Packet Routes

```plaintext
bashCopyEdittraceroute google.com  # Linux/macOS
tracert google.com  # Windows
```

✅ Shows the path packets take to reach the destination.

### **3️⃣** `netstat` - View Network Statistics

```plaintext
bashCopyEditnetstat -an
```

✅ Displays active connections & listening ports.

### **4️⃣** `curl` - Make HTTP Requests

```plaintext
bashCopyEditcurl -I https://example.com
```

✅ Fetches HTTP headers of a website.

### **5️⃣** `dig` / `nslookup` - DNS Lookup

```plaintext
bashCopyEditdig google.com  # Linux/macOS
nslookup google.com  # Windows
```

✅ Resolves a domain name to an IP address.

## **🔹 Conclusion**

By understanding **AWS EC2 Security Groups** and mastering **networking commands**, you can:  
✅ Secure cloud instances properly  
✅ Debug connectivity issues efficiently  
✅ Improve your DevOps & cloud skills