---
title: "🚀 Mastering Linux System Administration & Automation | 90 Days of DevOps - Week 2"
datePublished: Mon Feb 17 2025 09:50:01 GMT+0000 (Coordinated Universal Time)
cuid: cm78vjo8f000s0akyajrkgvbm
slug: mastering-linux-system-administration-and-automation-90-days-of-devops-week-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1739785673088/a9f52555-5ee0-44ac-a745-b0e5fd697959.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1739785772954/5492a262-f4ef-4229-af71-614ee7522c89.webp
tags: linux, devops, devops-journey, 90daysofdevops, tws, shellscripting-devops

---

## **Task 4 : Volume Management & Disk Usage**

### **4️⃣ Volume Management & Disk Usage**

* **Task:**
    
    * Create a directory `/mnt/devops_data`.
        
    * Mount a new volume (or loop device for local practice).
        
    * Verify using `df -h` and `mount | grep devops_data`.
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739783864976/5a9f502f-ba28-4651-91c0-c2045296825f.png align="center")

**Step 1: Create a Directory**

```bash
sudo mkdir -p /mnt/devops_data
```

*Why?* Directories are mount points for attaching storage.

**Step 2: Create a Loop Device (Virtual Disk)**

```bash
sudo dd if=/dev/zero of=/loop_devops.img bs=1M count=1024
sudo mkfs.ext4 /loop_devops.img
```

*Pro Tip:* `dd` creates raw binary files, while `mkfs` formats them.

**Step 3: Mount the Virtual Disk**

```bash
sudo mount -o loop /loop_devops.img /mnt/devops_data
```

**Verification:**

```bash
df -h | grep devops_data  # Check disk space
mount | grep devops_data  # Confirm mount details
```

```bash
/loop_devops.img  969M  2.6M  900M  1% /mnt/devops_data
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739783696887/39eeff83-869e-4f54-b8d5-3a01e9273757.png align="center")

## **Task 5 : Process Management & Monitoring**

### **5️⃣ Process Management & Monitoring**

* **Task:**
    
    * Start a background process (`ping` [`google.com`](http://google.com) `> ping_test.log &`).
        
    * Use `ps`, `top`, and `htop` to monitor it.
        
    * Kill the process and verify it's gone.
        

**Step 1: Start Background Process**

```bash
ping google.com > ping_test.log &
```

*Note:* `&` runs the process in the background.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739783795489/dac35e67-236a-446d-b88c-7cf432e37ee5.png align="center")

**Step 2: Monitor with CLI Tools**

* `ps`: `ps aux | grep ping`
    
* `top`: Interactive process viewer (sort with `Shift+M` for memory)
    
* `htop`: Colorful, user-friendly alternative (install via `sudo apt install htop`)
    

**Step 3: Terminate the Process**

```bash
kill -9 <PID>  # Replace with actual Process ID
pkill -f "ping google.com"  # Pattern-based kill
```

**Verification:**

```bash
ps aux | grep ping  # Should show only the grep command
ls -lh ping_test.log  # Check if file size stopped growing
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739783986919/dcc50273-c09e-48f3-af2d-740d43528ed6.png align="center")

### **6️⃣ Automate Backups with Shell Scripting**

* **Task:**
    
    * Write a shell script to back up `/devops_workspace` as `backup_$(date +%F).tar.gz`.
        
    * Save it in `/backups` and schedule it using `cron`.
        
    * Make the script display a success message in **green text** using `echo -e`.
        
* **Step 1 : Write a shell script to back up** `/devops_workspace` **as** `backup_$(date +%F).tar.gz`**.**
    

This is the shell script that can take a periodic backup of the scripts / directories and also uploads the backup to aws s3

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739783467158/dba9357f-b901-47d1-939f-5a6d13c76cbf.png align="center")

**Step 2 : Save it in** `/backups` **and schedule it using** `cron`**.**

I have scheduled a periodic backup for every minute. below is the example script for taking backup every minute.

write a command `crontab -e` to shcedule a cron.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739784245207/340272e4-a99d-4199-984b-281c888c8023.png align="center")

By Saving the above script, we have to enter a command `watch ls` this command shows the live page of the entered command

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1739784590653/003657c6-c1ea-4190-b12d-4c84e832082e.png align="center")

This above script displays the live backup process.

**🔥 Key Takeaways:  
**✔ Linux administration is the foundation of DevOps!  
✔ Automating tasks with shell scripting boosts efficiency.  
✔ Logs are gold for debugging and monitoring.  
✔ Managing users, processes, and storage is essential in production environments.