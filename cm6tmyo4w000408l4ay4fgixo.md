---
title: "Week-2 : Fundamentals of Linux OS for DevOps"
datePublished: Thu Feb 06 2025 17:53:12 GMT+0000 (Coordinated Universal Time)
cuid: cm6tmyo4w000408l4ay4fgixo
slug: week-2-fundamentals-of-linux-os-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738864283084/3d24b0c9-2dc0-4666-b236-afb28b6a9350.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1738864330120/2b23ced0-6aee-4fb3-9029-6e5af848c8d3.jpeg
tags: linux, devops, learning-in-public, 90daysofdevops-chanllenge, 90daysofdevopschallenge, tws

---

## **What is Operating System?**

An **Operating System (OS)** is system software that manages computer hardware and software resources. It provides a user interface and enables applications to run.

There are basically two types of OS we use,

## **🔹 Client OS**

A **Client Operating System** is designed for personal computers, laptops, or mobile devices. It provides a user-friendly interface and supports applications for day-to-day tasks.

### **Examples of Client OS:**

✅ **Windows** (Windows 10, Windows 11)  
✅ **Linux** (Ubuntu, Fedora)  
✅ **macOS**  

## **🔹Server OS**

A **Server Operating System** is designed to **manage network resources** and serve multiple clients. It runs on servers that host websites, applications, and databases.

Generally, used in the industrial purposes as it is a multi-user and multi-tasking.

### **Examples of Server OS:**

✅ **Windows Server** (Windows Server 2019, 2022)  
✅ **Linux Server** (Ubuntu Server, CentOS, Red Hat Enterprise Linux)  
✅ **macOS Server**

## Linux Basics

Linux is established by Linus Torvalds.

* It is open source
    
* multi-user & multi-tasking
    

Flavors of Linux : Ubuntu, CentOS, RedHat, Fedora

## Architecture of Linux

![Architecture ](https://cdn.hashnode.com/res/hashnode/image/upload/v1738860159887/ccd94070-f158-40a5-982b-a37b8c81d3ce.png align="center")

## **1\. Hardware Layer 🖥️**

* The **physical components** of the system (CPU, RAM, Hard Disk, Network Card, etc.).
    
* Linux interacts with hardware via device drivers.
    

## **2\. Kernel 🛠️ (Core of Linux)**

* The **heart of the OS**, directly communicating with hardware.
    
* Manages system resources like **CPU, memory, and devices**.
    
* Provides an interface for applications to interact with hardware.
    
* **Types of kernels in Linux:** Monolithic (Linux Kernel), Microkernel, Hybrid.
    

## **3\. Shell (Command Line Interface) 💻**

* Acts as a **bridge between the user and the kernel**.
    
* Users give commands using the shell (e.g., **Bash, Zsh**), which the kernel executes.
    

## **4\. Application Layer 🏗️**

* Where **user programs and applications** run (e.g., browsers, text editors, media players).
    
* Users interact with applications via **CLI (Command Line Interface)** or **GUI (Graphical User Interface)**.
    
    ## In Linux, “Everything is Directory or a File.”
    
    * / - Root Directory
        
* Root level linux directories
    
    1) Var (Variables) : Backup, cache, logs,…..etx
    
    2) tmp (temporary) : Everyone can access
    
    3) mnt (mount) : for stoarage adding
    
    4) home
    
    5) sbin : System level binary files
    
    6) Root : root user (handles the system
    
    7) etc : contains the configuration files
    
    8) bin : contains the all linux commands
    

### Some important linux commands,

* man : used to display the details of the commands
    
* cp : copy files
    
* mkdir : To make a new directory
    
* rm : remove files only
    
* rmdir : removes the directory
    
* rm -r : removes directory having files inside
    
* rm -v : remove files and show the message that “removed file\_name”
    
* vim : used for creating a files and opening file in in write mode for writing a text, message into it.
    

### Package manager : **apt** for ubuntu

* update : used to download the package. ( sudo apt-get update )
    
* upgrade : used to install the package. ( sudo apt-get upgrade )
    

**sudo (super user do) : It is a group that has a super user / root user permissions.**

## How to Install nginx server on Linux.

nginx :

* reverse proxy server
    
* generally used to host the web pages
    
* files of nginx are stored in the : /var
    

To install nginx on linux ,

```plaintext
sudo apt-get install nginx
```

To check , nginx is installed or check status of nginx

```plaintext
systemctl status nginx
```

**systemctl : tool that control the services that installed on the system**

To stop the nginx server.

```plaintext
sudo systemctl stop nginx
```

To start the nginx server.

```plaintext
sudo systemctl start ngnix
```

### **Conclusion**

Linux is a powerful, open-source OS widely used for both personal and server environments. Its architecture includes **Hardware, Kernel, Shell, and Application Layers**, making it secure, multi-user, and multi-tasking. Mastering Linux commands, directories, and package management is essential for system administration. Additionally, setting up **Nginx** for web hosting showcases its flexibility in managing servers. **Linux skills are crucial for DevOps, cloud computing, and automation!** 🚀