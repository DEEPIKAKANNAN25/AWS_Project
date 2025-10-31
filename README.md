# AWS_Project

🌐 AWS S3 Static Website Hosting – Personal Portfolio

🧭 Overview

This project demonstrates how to host a static personal portfolio website using Amazon S3.
It covers every step from bucket creation to website hosting and public access configuration — a simple yet powerful example of serverless website deployment on AWS.

☁️ What is Amazon S3?

Amazon Simple Storage Service (S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.
You can store and retrieve any amount of data from anywhere on the web.

🔹 Key Features

Unlimited data storage

High durability (99.999999999%)

Secure access control

Cost-effective pay-as-you-go pricing

Integrated with AWS services like CloudFront, Lambda, and QuickSight

🎯 Project Objective

To deploy a static portfolio website using Amazon S3, ensuring:

Public access for users to view the site globally

Reliable, scalable hosting without needing a web server

Step-by-step AWS implementation for beginners

🛠️ Services Used
AWS Service	Purpose
Amazon S3	Hosting the static website files
AWS Management Console	Creating and configuring resources
IAM	Managing user permissions (if required)
🧩 Step-by-Step Implementation
Step 1: Create an S3 Bucket

Go to the AWS Management Console → S3.

Click Create Bucket and give it a unique name.

Choose your region (e.g., Asia Pacific – Mumbai).

Uncheck Block all public access.

Click Create bucket.

Step 2: Verify the Created Bucket

Once created, verify the bucket in your S3 dashboard to ensure it appears under your list of buckets.

Step 3: Upload Website Files

Open your bucket → Objects tab → click Upload.

Upload the following files:

index.html

style.css

script.js

Click Upload to confirm.

Step 4: Enable Static Website Hosting

Go to Properties → Static website hosting.

Enable it and set:

Index document: index.html


Save changes — this generates your website endpoint.

Step 5: Set Bucket Policy for Public Access

Go to Permissions → Bucket Policy and add the following:

<img width="783" height="445" alt="image" src="https://github.com/user-attachments/assets/438435b5-67f9-40f2-bf98-dded1dc62dd5" />



Replace your-bucket-name with your actual S3 bucket name.

Step 6: Disable Block Public Access

In the Permissions tab, scroll to Block public access (bucket settings).

Turn off “Block all public access”.

Type confirm and save changes.

Step 7: Verify and Access the Website

Copy the Website endpoint URL from Static website hosting.

Paste it into your browser — your website is now live 🎉

Example:

http://personal-portfolio-website-hosting.s3-website.ap-south-1.amazonaws.com
📸 Implementation Screenshots

Below are all 22 screenshots showing the full implementation process:

Screenshot	Description

	Opening the Amazon S3 console and clicking “Create bucket”.

	Entering bucket name and region details.

	Configuring permissions and access settings.

	Finalizing and creating the S3 bucket.

	Successfully created S3 bucket displayed in the console.

	Opening the bucket to view configuration tabs.

	Uploading index.html, style.css, and script.js.

	Upload process confirmation window.

	Uploaded files listed under S3 bucket objects.

	Successful upload confirmation message.

	Accessing the Properties tab.

	Locating the Static website hosting section.

	Enabling static website hosting.

	Saving hosting settings and generating website endpoint.

	Opening Permissions settings.

	Editing bucket policy for public access.

	Reviewing policy details.

	Confirming the updated bucket policy.

	Accessing block public access section.

	Confirming public access configuration.

	Viewing the generated website endpoint.

	Final hosted portfolio website successfully accessible.

📁 Tip: Place all screenshots in a folder named /images inside your GitHub repository.

🎥 Demo Video

🎬 Watch the complete project walkthrough here:


Replace VIDEO_ID with your actual YouTube video ID.

🌟 Benefits of Hosting on Amazon S3

Scalable: Automatically handles traffic fluctuations

Secure: Fine-grained access control using IAM and policies

Serverless: No need to manage infrastructure

Cost-efficient: Pay only for the storage and data you use

Highly Available: 99.99% uptime and global accessibility

📚 Conclusion

By completing this project, you have:

Learned to deploy a static website on Amazon S3

Understood key AWS configurations for public access

Created a serverless, scalable, and secure portfolio website

This project demonstrates the power of AWS S3 as a hosting solution — ideal for portfolios, resumes, documentation, and lightweight web apps.
