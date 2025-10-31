🌐 AWS S3 Static Website Hosting – Personal Portfolio

🧭 Overview

This project demonstrates how I hosted a static website (my personal portfolio) on Amazon S3, a scalable and cost-effective cloud storage service. It covers creating an S3 bucket, configuring it for public access, uploading website files, and enabling static website hosting. The result is a live, serverless website accessible via a public URL.

What is Amazon S3?

Amazon Simple Storage Service (S3) is a highly durable, scalable, and secure object storage service from AWS. It allows me to store and retrieve data from anywhere on the web. Key features include:

Highly Scalable: Handles large amounts of data with automatic scaling.

Durable: 99.999999999% (11 9's) durability for stored objects.

Secure: Supports encryption, access controls, and compliance standards.

Cost-Effective: Pay only for what I use, with low storage and transfer costs.

Seamless Integration: Works with AWS services like CloudFront, Lambda, and QuickSight.

🔹Key Features of S3 for Static Website Hosting

Serverless: No need for servers or infrastructure management.

Global Reach: Content delivered via AWS edge locations for low latency.

Highly Available: 99.99% uptime SLA with global reach via AWS edge locations.

Customizable: Supports custom domains, HTTPS (via CloudFront), and more.

Easy to Use: Simple setup through the AWS Management Console.

🎯 Project Objective

The goal was to build and deploy my personal portfolio website using AWS S3. This included:

Creating and configuring an S3 bucket for public access.

Uploading static files (HTML, CSS, JS, images).

Enabling static website hosting.

Testing the live site.

🛠️AWS Services Used

Amazon S3: For storage and hosting.

AWS Management Console: For setup and configuration.

🧩 Step-by-Step Implementation

The entire implementation process has been divided into five structured parts to ensure clarity and a smooth workflow.
Each part focuses on a key stage of the project — from creating the S3 bucket to verifying the final hosted website.
Screenshots are provided for every step to visually demonstrate the actions performed in the AWS Management Console.

Part 1: S3 Bucket Creation

Part 2: Bucket Policy Configuration

Part 3: Static Website Hosting Setup

Part 4: File Upload and Management

Part 5: Website Preview and Verification

This division makes it easier to follow the process sequentially and understand the purpose of each configuration made in AWS S3.


🪣 Part 1 – S3 Bucket Creation (Screenshots 1–7)

🖼️ 1. Bucket Name Setup ([images/1-bucket-name.png](images/1-bucket-name.png))

            Description:This step shows the creation of a new S3 bucket. You must enter a globally unique bucket name (e.g., my-portfolio-bucket-demo).

             Key Setting:Choose the AWS Region close to your target audience to minimize latency.

🖼️ 2. Object Ownership Configuration ([images/2-object-ownership.png](images/2-object-ownership.png))

             Description:Configure who owns and manages uploaded objects in the bucket.

             Best Practice:Select Bucket owner enforced to ensure the bucket owner controls all objects (helps with access consistency).

🖼️ 3. Block Public Access Settings ([images/3-block-public-access.png](images/3-block-public-access.png))

             Description:AWS blocks public access by default for security.

             Action:Uncheck Block all public access if your goal is to host a public website.

             Warning:Only disable this if you understand the implications — this bucket will be readable by the public.

🖼️ 4. Versioning Configuration ([images/4-versioning-settings.png](images/4-versioning-settings.png))

             Description:Versioning helps you keep multiple versions of an object (useful for rollback).

             Optional:Enable versioning for production environments; it’s not mandatory for static websites.

🖼️ 5. Encryption Type Selection ([images/5-encryption-type.png](images/5-encryption-type.png))

              Description:You can choose to encrypt your data at rest using Amazon S3-managed keys (SSE-S3) or AWS KMS keys (SSE-KMS).

               Best Practice:Use SSE-S3 for simplicity unless compliance requires KMS.

🖼️ 6. Create Bucket Confirmation ([images/6-create-bucket.png](images/6-create-bucket.png))

             Description:This screenshot confirms clicking the Create bucket button at the bottom of the page.

             Outcome:A new bucket is successfully created with the specified configuration.

🖼️ 7. Bucket Created Successfully ([images/7-object-created-success-message.png](images/7-object-created-success-message.png))

             Description:AWS confirms that your bucket has been created.

             Next Step:Click the bucket name to open it and configure it for website hosting.

🔐 Part 2 – Bucket Policy Configuration (Screenshots 8–9)

🖼️ 8. Add Policy JSON Document ([images/8-policy-json-document.png](images/8-policy-json-document.png))

          Description:In the Permissions tab, add a Bucket Policy that grants public read access to objects.

          Purpose:This allows anyone on the internet to access the files hosted in your S3 bucket.

          

<img width="891" height="347" alt="image" src="https://github.com/user-attachments/assets/4a90227e-b5d7-431d-acd0-e97ed40b8ed3" />



🖼️ 9. Policy Applied Successfully ([images/9-policy-success-message.png](images/9-policy-success-message.png))

         Description:This screenshot confirms that the JSON policy was accepted and applied.

         Verification:The bucket should now allow public access to its objects (useful for hosting a static website).

🌐 Part 3 – Static Website Hosting Setup (Screenshots 10–13)

🖼️ 10. Enable Static Website Hosting ([images/10-static-website-hosting.png](images/10-static-website-hosting.png))

           Description:Go to the Properties tab and scroll to Static website hosting.

           Action:Enable hosting and specify your index document (e.g., index.html) and error document (e.g., error.html).

🖼️ 11. Hosting Success Message ([images/11-hosting-success-message.png](images/11-hosting-success-message.png))

            Description:Confirms that static hosting has been enabled successfully.

            Outcome:AWS provides an endpoint URL for your hosted site, usually like:

             http://my-portfolio-bucket-demo.s3-website-us-east-1.amazonaws.com

🖼️ 12. Website URL Displayed ([images/12-website-url.png](images/12-website-url.png))

              Description:This shows the generated website endpoint.

              Action:Copy this URL to test your hosted site in a browser.

🖼️ 13. Custom Error Page ([images/13-error-page.png](images/13-error-page.png))

              Description:Displays your custom error page when a non-existent page is requested.

              Purpose:Provides a professional user experience even for invalid URLs.

☁️ Part 4 – File Upload and Management (Screenshots 14–18)

🖼️ 14. Upload Page Interface ([images/14-upload-page.png](images/14-upload-page.png))

               Description:Click Upload to start adding your website files (HTML, CSS, JS, images) into the bucket.

🖼️ 15. File Upload Interface ([images/15-file-upload-page.png](images/15-file-upload-page.png))

             Description:Shows the file selection dialog where you choose your local files to upload.

             Best Practice:Maintain the same folder structure as your website project.

🖼️ 16. List of Uploaded Files ([images/16-uploaded-files-list.png](images/16-uploaded-files-list.png))

            Description:Displays all files uploaded to your S3 bucket.

            Verification:Ensure index.html and error.html exist at the root level.

🖼️ 17. Files Uploading in Progress ([images/17-files-uploading.png](images/17-files-uploading.png))

             Description:Indicates that the upload process is ongoing.

             Tip:Large files might take longer depending on your internet speed.

🖼️ 18. Upload Success Confirmation ([images/18-upload-success-message.png](images/18-upload-success-message.png))

             Description:Confirms all website files were uploaded successfully.

             Next Step:Visit your static website endpoint to view your hosted site.

🧭 Part 5 – Website Preview Pages (Screenshots 19–21)

🖼️ 19. About Page ([images/19-static-webiste-about.png](images/19-static-webiste-about.png))

             Description:Displays the “About, Education and Experience” section of the hosted static website captured during page scrolling.

🖼️ 20. Projects Page ([images/20-static-website-projects.png](images/20-static-website-projects.png))

               Description:Shows the “Projects” section of the website while scrolling through the hosted static site.

🖼️ 21. Certificates Page ([images/21-static-website-certificates.png](images/21-static-website-certificates.png))

               Description:Shows the “Technical skills, Soft skills and Certificates” section of the website while scrolling through the hosted static site.

🎥 Demo Video: A full walkthrough of the deployed website in action: https://github.com/DEEPIKAKANNAN25/AWS_Project/blob/main/Project-Demo/VideoRecording.mp4

🌟 Benefits of Hosting on Amazon S3

 • Scalable: Handles high traffic automatically

 • Secure: IAM and bucket policies for access control

 • Serverless: No infrastructure management needed

 • Cost-effective: Pay only for what you use

 • Highly Available: 99.99% uptime with global reach

📚 Conclusion

 • By completing this project, I:

 • Gained hands-on experience deploying a static website on AWS S3

 • Learned how to configure public access and bucket policies

 • Built a secure, scalable, and serverless portfolio site

 • This project is a great example of using AWS S3 for lightweight web hosting — perfect for portfolios, resumes, documentation, and more.
