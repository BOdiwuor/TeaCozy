# Tea Cozy Website – Project Documentation

---

## Learning Journey
Over the past year, I built a foundation in **HTML, CSS, and basic JavaScript**, creating static web pages to practice and test my skills. Initially, I shared my pages with peers to gather feedback and refine my work.

This year, I explored ways to make my static websites **publicly accessible in a secure and efficient manner**. Since AWS powers a large portion of the internet, I began learning how to host webpages using **AWS services** through **AWS Skill Builder**, gaining hands-on experience with **EC2, S3, and web security best practices**. This allowed me to understand how to deploy web pages that are accessible 24/7 while considering **cost-effectiveness and scalability**.

---

## Project Purpose
The **Tea Cozy Website** is a static fictional website designed to showcase the types of tea offered by the tea shop “Tea Cozy.”

---

## Languages Used
- **HTML**  
- **CSS**

---

## Business Problem
The webpage was only accessible if the link was shared by the owner. The business needed the website to be **publicly accessible** and live on the internet **24/7**.

---

## Solution

### AWS EC2 Hosting
- Hosted the static website on an **EC2 instance** to make it publicly accessible while the instance is running.  
- Configured **security groups** and network settings to allow web traffic from the internet.  

### AWS S3 Exploration
After hosting the website on EC2, I explored **Amazon S3** as a solution for static websites. Since the Tea Cozy website is fully static, S3 is particularly suited for this use case because:  

- It **does not involve server management tasks** (no OS management, patching, or scaling required).  
- It is **designed specifically for static sites**.  
- It **auto-scales instantly** to handle any number of requests.  
- It **behaves as a web server** for static content.  
- It **does not run in a VPC**, meaning it is a public AWS-managed service separate from private networks.  

I copied the HTML and CSS files into an **S3 bucket** and configured it for **public read-only access**, allowing users to view the site. While S3 alone does not provide HTTPS directly (causing the “Not Secure” warning in browsers), it is an excellent option for learning static hosting fundamentals and AWS best practices.  

Since my AWS account was **not verified** at the time (the verification process took longer than expected), I received an **error when attempting to create a CloudFront distribution**. However, I documented how **CloudFront with Origin Access Control (OAC)** can be used to serve content over HTTPS while keeping the bucket private, demonstrating secure production hosting best practices.

---

## Outcome
- Gained hands-on experience with **EC2, S3, bucket policies, and AWS security considerations**.  
- Demonstrated understanding of **static website hosting, HTTPS limitations, and AWS-recommended secure delivery methods**.  
- Showcased ability to deploy static websites on **multiple AWS services** and explain trade-offs between hosting options.

---
