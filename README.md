
🌐 AWS S3 Static Website Hosting – Personal Portfolio

🧭 Overview

In this project, I hosted my static personal portfolio website using Amazon S3. It walks through the complete process—from creating an S3 bucket to configuring public access and enabling static website hosting. This is a beginner-friendly example of deploying a serverless website on AWS.

☁️ What is Amazon S3?

Amazon S3 (Simple Storage Service) is a highly scalable and durable object storage service provided by AWS. It allows users to store and retrieve any amount of data from anywhere on the web, making it ideal for hosting static websites.

🔹 Key Features of S3
Unlimited data storage

99.999999999% durability

Fine-grained access control

Pay-as-you-go pricing model

Seamless integration with AWS services like CloudFront, Lambda, and QuickSight

🎯 Project Objective
The goal was to deploy a static portfolio website using Amazon S3 with the following outcomes:

Enable public access for global visibility

Achieve scalable and reliable hosting without managing servers

Provide a clear, step-by-step AWS implementation suitable for beginners

🛠️ AWS Services Used
Amazon S3

IAM (for bucket policy)

(Optional) CloudFront for CDN integration

🧩 Step-by-Step Implementation
✅ Step 1: Create an S3 Bucket
Logged into AWS Management Console → S3

Clicked “Create Bucket” and gave it a unique name

Selected region: Asia Pacific (Mumbai)

Unchecked “Block all public access”

Clicked “Create bucket”

✅ Step 2: Verify the Created Bucket
Confirmed the bucket was listed in the S3 dashboard

✅ Step 3: Upload Website Files
Navigated to the bucket → Objects tab → Clicked “Upload”

Uploaded index.html, style.css, and script.js

Clicked “Upload” to confirm

✅ Step 4: Enable Static Website Hosting
Went to Properties → Enabled “Static website hosting”

Set index document as index.html

Saved changes to generate the website endpoint

✅ Step 5: Set Bucket Policy for Public Access
Opened Permissions → Bucket Policy

Added a JSON policy to allow public read access

Replaced your-bucket-name with my actual bucket name

json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
✅ Step 6: Disable Block Public Access
In Permissions tab → Scrolled to “Block public access”

Disabled “Block all public access”

Typed “confirm” and saved changes

✅ Step 7: Verify and Access the Website
Copied the website endpoint URL from the Static website hosting section

Pasted it into the browser — the portfolio website was live 🎉

Example URL: http://personal-portfolio-website-hosting.s3-website.ap-south-1.amazonaws.com

📸 Implementation Screenshots
(Screenshots of each step were captured and added to the GitHub repository for visual reference.)

🎥 Demo Video
Watch the full walkthrough here: https://www.youtube.com/watch?v=VIDEO_ID (Replace with actual video ID)

🌟 Benefits of Hosting on Amazon S3
Scalable: Handles high traffic automatically

Secure: IAM and bucket policies for access control

Serverless: No infrastructure management needed

Cost-effective: Pay only for what you use

Highly Available: 99.99% uptime with global reach

📚 Conclusion
By completing this project, I:

Gained hands-on experience deploying a static website on AWS S3

Learned how to configure public access and bucket policies

Built a secure, scalable, and serverless portfolio site

This project is a great example of using AWS S3 for lightweight web hosting — perfect for portfolios, resumes, documentation, and more.
