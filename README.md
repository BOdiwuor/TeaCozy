# Tea Cozy Website – Project Documentation

---

## Learning Journey
Over the past year, I built a foundation in **HTML, CSS, and basic JavaScript** by creating static web pages to practice and test my skills. Initially, I shared these pages with peers for feedback and refinement.

This year, I explored ways to make my static websites **publicly accessible in a secure and efficient manner**. Leveraging **AWS**, I gained hands-on experience with **EC2, S3**, and **web security best practices** through the **AWS Skill Builder** platform. This journey helped me understand how to deploy websites that are **accessible 24/7** while being **cost-effective and scalable**.

---

## Project Purpose
The **Tea Cozy Website** is a fictional static website designed to showcase the variety of teas offered by the tea shop “Tea Cozy.”

---

## Languages Used
- **HTML**  
- **CSS**

---

## Business Problem
Previously, the website was only accessible through a shared link from the owner. The business needed a solution to make the website **publicly available** and **live 24/7** for all visitors.

---

## Solution

### AWS EC2 Hosting
I initially hosted the website on an **EC2 instance** to make it publicly accessible while the instance was running. This solution required:

- Configuring **security groups** and network settings to allow web traffic from the internet.
- Running an **Nginx server** to serve the static files.

However, EC2 instances incur costs even when idle, making it an expensive solution in the long run. Since the Tea Cozy website is static, I looked for a more cost-effective option.

### AWS S3 Exploration
I then explored **Amazon S3** for hosting static websites. Since the Tea Cozy website is fully static, **S3** proved to be a great fit because:

- **No server management**: No OS maintenance, patching, or scaling required.
- **Auto-scaling**: Handles any number of requests automatically.
- **Cost-effective**: A fraction of the cost of EC2 for serving static files.
- **Public access**: Behaves as a web server for static content without running in a VPC.

I copied the HTML and CSS files into an **S3 bucket** and configured it for **public read-only access**, allowing users to access the site. Although **S3** does not provide HTTPS by default, it’s an excellent platform for static websites.

However, since my **AWS account wasn’t verified** (the process took longer than expected), I received an error when trying to create a **CloudFront distribution**. 

---

## Outcome
- Gained hands-on experience with **EC2**, **S3**, **bucket policies**, and **AWS security best practices**.
- Demonstrated an understanding of **static website hosting**, **HTTPS limitations**, and **AWS-recommended secure delivery methods**.
- Showcased the ability to deploy websites across **multiple AWS services** while explaining the **trade-offs** between hosting solutions.


