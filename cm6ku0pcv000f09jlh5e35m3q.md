---
title: "Beginner’s Guide to OSI & TCP/IP Models ( With Real-World Examples )"
datePublished: Fri Jan 31 2025 14:00:48 GMT+0000 (Coordinated Universal Time)
cuid: cm6ku0pcv000f09jlh5e35m3q
slug: beginners-guide-to-osi-tcpip-models-with-real-world-examples
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738331585447/3ef89530-8308-4b5a-9db5-3762f37c478e.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1738332020190/f63a915e-cf82-4ba3-8796-76c5b6adff4c.jpeg
tags: devops, networking, learning-in-public, 90daysofdevops, 90daysofdevops-chanllenge, tws

---

Have you ever wondered how the internet actually works? How does your message on WhatsApp get delivered? How does your laptop communicate with a website?

Well, that’s where **networking models** come in. The **OSI and TCP/IP models** break down how data travels over the internet in a structured way. Don't worry—I’ll explain it in the simplest way possible with **real-world examples** that actually make sense.

## What Are OSI & TCP/IP Models?

Think of networking like **sending a package through a courier service**. You don’t just throw a parcel in the air and hope it reaches your friend, right? There’s a process:

1. You pack the item.
    
2. You write the address.
    
3. A delivery person picks it up.
    
4. The package goes through sorting centers.
    
5. It’s transported (by truck, plane, etc.).
    
6. A local courier delivers it.
    
7. Your friend receives and opens it.
    

The **OSI model** does the same thing—but for data traveling across the internet. It splits the process into **seven layers**, each handling a different job.

The **TCP/IP model**, on the other hand, is the simplified **real-world version** that powers the internet today.

## The OSI Model (7 Layers Explained Simply)

### **1️⃣ Physical Layer – The Wires & Signals**

📌 **What it does?** It’s the actual hardware—cables, Wi-Fi signals, and radio waves—that send raw data (bits).

💡 **Real-life example:** Your internet cable, Wi-Fi router, or Bluetooth connection.

👉 **Example:** When you connect to Wi-Fi at a café, your device communicates with the router using radio waves—this is the physical layer in action!

### **2️⃣ Data Link Layer – Direct Device Communication**

📌 **What it does?** It makes sure data is sent between two directly connected devices **without errors**.

💡 **Real-life example:** **MAC addresses** (a unique ID for every device), network switches, Ethernet.

👉 **Example:** When two laptops in an office share files over a local network, the data link layer ensures they talk correctly.

### **3️⃣ Network Layer – Finding the Best Path (IP Addressing & Routing)**

📌 **What it does?** It figures out the best way to send data across different networks using **IP addresses**.

💡 **Real-life example:** **Routers, IP addresses, the internet itself.**

👉 **Example:** When you visit [**Google.com**](http://Google.com), your request travels through routers, which forward it to Google’s server using its **IP address**.

### **4️⃣ Transport Layer – Reliable Delivery (TCP & UDP)**

📌 **What it does?** It makes sure data arrives **completely and in order**, even if some packets get lost. Uses **TCP (reliable)** or **UDP (fast but unreliable)**.

💡 **Real-life example:**

* **TCP** (WhatsApp messages, web browsing – ensures accuracy).
    
* **UDP** (Live streams, video calls – prioritizes speed over accuracy).
    

👉 **Example:** When you send a WhatsApp message, **TCP** ensures it reaches your friend **correctly and in order**, even if there’s a network issue.

### **5️⃣ Session Layer – Keeping Connections Alive**

📌 **What it does?** It manages **sessions**—meaning it keeps a communication channel open while you’re using it.

💡 **Real-life example:** **Logging into a website, Zoom calls, database connections.**

👉 **Example:** When you’re on a Zoom call, the session layer ensures your connection stays active until you leave the meeting.

### **6️⃣ Presentation Layer – Formatting & Encryption**

📌 **What it does?** It **translates, compresses, and encrypts** data so different systems can understand it.

💡 **Real-life example:** **SSL encryption (HTTPS), file compression (JPEG, MP3), text encoding (ASCII, Unicode).**

👉 **Example:** When you stream a song on **Spotify**, the music is compressed into MP3 format so it loads faster without losing quality.

### **7️⃣ Application Layer – The User’s Experience**

📌 **What it does?** This is where you **interact with apps** like browsers, email clients, and messaging services.

💡 **Real-life example:** **Web browsing (HTTP/HTTPS), Email (SMTP, IMAP), Cloud services (Google Drive).**

👉 **Example:** When you send an email, the application layer (SMTP) handles it and sends it to the recipient’s inbox.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738329430855/6c0ccca9-e01a-4115-86ed-f27c9f4325a0.jpeg align="center")

## **The TCP/IP Model (The Real-World Version)**

The **TCP/IP model** is what we actually use today—it simplifies the OSI model into **four layers** instead of seven.

### 1️⃣ **Application Layer**

Handles user-facing apps and services. Example: WhatsApp (Messaging), Chrome (Web), Gmail (Email).

### 2️⃣ **Transport Layer** –

Ensures reliable or fast data delivery. Example: TCP (WhatsApp messages for accuracy), UDP (Netflix streaming for speed).

### 3️⃣ **Internet Layer**

Manages routing and IP addresses. Example: Routers and IP addressing help data packets find their destination.

### 4️⃣ **Network Access Layer**

Deals with physical data transfer. Example: Wi-Fi, Ethernet, and mobile networks ensure data moves across devices.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738331611081/25b91671-bc14-4fe6-b03a-0ab25eff1b2f.png align="center")

## **How This Works in Real Life (Example: Opening a Website)**

Let’s say you **open** [**Google.com**](http://Google.com) on your browser. Here’s how the **TCP/IP layers** work together:

1️⃣ **Application Layer** → Your browser sends an HTTP request.  
2️⃣ **Transport Layer** → TCP breaks the request into small packets.  
3️⃣ **Internet Layer** → The packets are sent to Google’s server using IP addresses.  
4️⃣ **Network Access Layer** → The request travels via Wi-Fi or Ethernet to reach the internet.

Google’s server then **sends back the webpage**, and your browser displays it.

## Why Should You Care About This?

* If you’re into **DevOps, cloud computing, or cybersecurity**, understanding networking is **critical**.
    
* It helps you troubleshoot **slow internet, failed connections, and security issues**.
    
* These models are the **foundation of the internet**—knowing them makes you **tech-savvy**.
    

💡 **In short, OSI is the blueprint, TCP/IP is the real-world version, and together, they make the internet work!** 🚀

### **Final Thoughts**

If you made it this far, congrats! 🎉 You now have a **solid understanding** of OSI & TCP/IP models **without the boring technical jargon**.

👉 **Did this guide help?** Let me know if you have any questions! 😊