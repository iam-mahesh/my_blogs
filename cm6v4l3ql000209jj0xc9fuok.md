---
title: "Week-2 : Advanced Linux for devops"
datePublished: Fri Feb 07 2025 18:54:18 GMT+0000 (Coordinated Universal Time)
cuid: cm6v4l3ql000209jj0xc9fuok
slug: week-2-advanced-linux-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738954369037/a6eb72a1-1ce0-42da-b598-4a154399edbb.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1738954438671/233064d3-f454-45c2-91a9-6655b28b210f.jpeg
tags: linux, aws, devops, 90daysofdevops, 90daysofdevops-chanllenge, tws

---

## **1\. What Are Users & Groups?**

### 👤 **Users**

* Every person using the system is a **user**.
    
* Each user has a **User ID (UID)** and a **home directory**.
    
* The **root user (UID 0)** has full system control.
    

### 🏷️ **Groups**

* A **group** is a collection of users with shared permissions.
    
* Users belong to a **primary group** and can be part of multiple **secondary groups**.
    

## **2\. User Management**

### ✅ **Create a New User**

```plaintext
sudo useradd -m devopsuser  # Creates a user with a home directory
sudo passwd devopsuser      # Sets a password for the user
```

### 🔄 **Modify a User**

```plaintext
sudo usermod -aG docker devopsuser  # Add user to the "docker" group
sudo usermod -l newname oldname     # Rename a user
sudo usermod -d /new/home username  # Change home directory
```

### ❌ **Delete a User**

```plaintext
sudo userdel -r devopsuser  # Removes the user and their home directory
```

## 3\. Groups in Linux

In Linux, **groups** are used to manage user permissions and access control. A group is a collection of users who share the same permissions for files, directories, or system resources.

### **Types of Groups in Linux**

1. **Primary Group** – Each user has a primary group, which is usually created with the same name as the username. Files created by the user belong to this group by default.
    
2. **Secondary (Supplementary) Group** – Users can be part of multiple secondary groups, allowing them to access shared files and directories.
    

### **Common Group Commands**

✅ **Check your groups:**

```plaintext
bashCopyEditgroups
```

✅ **List all groups in the system:**

```plaintext
bashCopyEditcat /etc/group
```

✅ **Add a new group:**

```plaintext
bashCopyEditsudo groupadd mygroup
```

✅ **Add a user to a group:**

```plaintext
bashCopyEditsudo usermod -aG mygroup username
```

✅ **Remove a user from a group:**

```plaintext
bashCopyEditsudo gpasswd -d username mygroup
```

✅ **Delete a group:**

```plaintext
bashCopyEditsudo groupdel mygroup
```

### **Why Use Groups?**

🔹 Helps in managing file permissions easily  
🔹 Allows multiple users to collaborate on shared files  
🔹 Enhances security by restricting access

## 📌Task - 1 of the Linux as part of #90DaysOfDevOps Challenge.

### **1️⃣ User & Group Management**

* Learn about Linux **users, groups, and permissions** (`/etc/passwd`, `/etc/group`).
    
* **Task:**
    
    * Create a user `devops_user` and add them to a group `devops_team`.
        
    * Set a password and grant **sudo** access.
        
    * Restrict SSH login for certain users in `/etc/ssh/sshd_config`.
        
* **Task Solution:**
    
    **1) Create a user** `devops_user` **and add them to a group** `devops_team`**.**
    
    * To create a user in linux, we use “useradd” command
        
    
    ```plaintext
    sudo useradd -m devops_user  ( -m : creates the users home directory)
    ```
    
    2) Create a group devops\_team
    
    * To create a group in linux, we use “groupadd” command.
        

```plaintext
    sudo groupadd devops_team
```

3) Add a devops\_user to the devops\_team group

* we use the “usermod” command to add the existing user to group
    
* \- aG : Appends the user to the group without removing them from other group
    

```plaintext
sudo usermod -aG devops_team devops_user 
```

4) set a password for a devops\_user

* To set password for a user, we use the “passwd” command.
    

```plaintext
sudo passwd devops-user    #( you will be promted to enter password and confirm.)
```

5) Grant sudo access to devops\_user

* we need, to edit the sudoers file to grant devops\_user sudo access.
    
    ```plaintext
    sudo usermod -aG sudo devops_user   #(-aG sudo : add devops_user to sudo group) 
    ```
    

6) Restrict SSH login for certain users in `/etc/ssh/sshd_config`.

* To restrict the ssh login for certain user, we will need to modify the /etc/ssh/sshd\_config file.
    
* **steps:**
    
* **open the ssh configuration file**
    
* sudo vim /etc/ssh/sshd\_config file.
    
* To denu ssh access for a specific users, we need to add following line
    
* DenyUsers user1 user2
    
    Replace the username user1, user2 the name of user you want to deny access
    
    for example : DenyUsers devops\_user
    
* Allow access for certain users ( if needed ) : AllowUsers devops\_user
    
* save and exit the file
    
* Restart the ssh service for the changes to take effect
    
* sudo systemctl restart sshd