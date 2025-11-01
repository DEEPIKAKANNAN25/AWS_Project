🌐** AWS S3 Static Website Hosting – Personal Portfolio**

🧭 Overview

This project demonstrates how I hosted a static website (my personal portfolio) on Amazon S3, a scalable and cost-effective cloud storage service. It covers creating an S3 bucket, configuring it for public access, uploading website files, and enabling static website hosting. The result is a live, serverless website accessible via a public URL.

🗄️ What is Amazon S3?

Amazon Simple Storage Service (S3) is a highly durable, scalable, and secure object storage service from AWS. It allows me to store and retrieve data from anywhere on the web. Key features include:

Highly Scalable: Handles large amounts of data with automatic scaling.

Durable: 99.999999999% (11 9's) durability for stored objects.

Secure: Supports encryption, access controls, and compliance standards.

Cost-Effective: Pay only for what I use, with low storage and transfer costs.

Seamless Integration: Works with AWS services like CloudFront, Lambda, and QuickSight.

🔹 Key Features of S3 for Static Website Hosting

Serverless: No need for servers or infrastructure management.

Global Reach (with CloudFront integration): S3 can be combined with CloudFront CDN for faster global delivery.

Highly Available: 99.99% uptime.

Customizable: Supports custom domains, HTTPS (via CloudFront), and more.

Easy to Use: Simple setup through the AWS Management Console.

🎯 Project Objective

The goal was to build and deploy my personal portfolio website using AWS S3. This included:

Creating and configuring an S3 bucket for public access.

Uploading static files (HTML, CSS, JS, images).

Enabling static website hosting.

Testing the live site.

🛠️ AWS Services Used

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

This structure makes it easier to follow the process step-by-step and understand each AWS S3 configuration.


1️⃣ Part 1 – S3 Bucket Creation (Screenshots 1–7)

🖼️ 1. Bucket Name Setup ([images/1-bucket-name.png](images/1-bucket-name.png))

I logged in to the AWS Management Console, navigated to S3, and clicked "Create bucket". I entered a unique bucket name (personal-portfolio-website-hosting) and selected a region.

Key Setting: Choose the AWS Region close to your target audience to minimize latency.

🖼️ 2. Object Ownership Configuration ([images/2-object-ownership.png](images/2-object-ownership.png))

I selected "Bucket owner enforced" to ensure the bucket owner controls all objects. This helps with access consistency.

🖼️ 3. Block Public Access Settings ([images/3-block-public-access.png](images/3-block-public-access.png))

I unchecked "Block all public access" since my goal was to host a public website.

⚠️ Warning: Only disable this for public websites, as it allows global read access. Ensure your bucket policy is restrictive to avoid security risks. For better security, limit public access to only the necessary objects.
🖼️ 4. Versioning Configuration ([images/4-versioning-settings.png](images/4-versioning-settings.png))

I enabled versioning for backup and recovery (optional but recommended).

🖼️ 5. Encryption Type Selection ([images/5-encryption-type.png](images/5-encryption-type.png))

I enabled server-side encryption (SSE-S3) for security.

🖼️ 6. Create Bucket Confirmation ([images/6-create-bucket.png](images/6-create-bucket.png))

I reviewed the settings and created the bucket.

🖼️ 7. Bucket Created Successfully ([images/7-object-created-success-message.png](images/7-object-created-success-message.png))

After creation, I clicked the bucket name to open its dashboard.

2️⃣ Part 2 – Bucket Policy Configuration (Screenshots 8–9)

🖼️ 8. Add Policy JSON Document ([images/8-policy-json-document.png](images/8-policy-json-document.png))

I went to the "Permissions" tab in the bucket dashboard. I added a policy to grant public read access to objects. This allows the website to be viewed publicly.

<img width="891" height="347"  alt="Bucket policy JSON example"  src="https://github.com/user-attachments/assets/4a90227e-b5d7-431d-acd0-e97ed40b8ed3" />

🖼️ 9. Policy Applied Successfully ([images/9-policy-success-message.png](images/9-policy-success-message.png))

The policy was applied to the bucket successfully.

3️⃣ Part 3 – Static Website Hosting Setup (Screenshots 10–13)

🖼️ 10. Enable Static Website Hosting ([images/10-static-website-hosting.png](images/10-static-website-hosting.png))

I navigated to the "Properties" tab. I enabled static website hosting, set the index document (e.g., "index.html"), and noted the endpoint URL (e.g., http://my-bucket.s3-website-us-east-1.amazonaws.com). S3 static websites use HTTP by default. For production, consider integrating CloudFront for HTTPS and custom domains.

🖼️ 11. Hosting Success Message ([images/11-hosting-success-message.png](images/11-hosting-success-message.png))

The success message is displayed at top.

🖼️ 12. Website URL Displayed ([images/12-website-url.png](images/12-website-url.png))

This shows the generated website endpoint. Copy this URL to test your hosted site in a browser.

🖼️ 13. Custom Error Page ([images/13-error-page.png](images/13-error-page.png))

Displays a custom error page when a non-existent page is requested. 

4️⃣ Part 4 – File Upload and Management (Screenshots 14–18)

🖼️ 14. Upload Page Interface ([images/14-upload-page.png](images/14-upload-page.png))

I went to the "Objects" tab for uploading.

🖼️ 15. File Upload Interface ([images/15-file-upload-page.png](images/15-file-upload-page.png))

I uploaded my static files (HTML, CSS, JS, images) by clicking "Upload". I selected all required website files.
              
🖼️ 16. List of Uploaded Files ([images/16-uploaded-files-list.png](images/16-uploaded-files-list.png))

This screen showed the list of selected files before confirming upload.

🖼️ 17. Files Uploading in Progress ([images/17-files-uploading.png](images/17-files-uploading.png))

This showed the process of file uploads.

🖼️ 18. Upload Success Confirmation ([images/18-upload-success-message.png](images/18-upload-success-message.png))

This confirmed that all website files were uploaded successfully. I visited the static website endpoint to view the hosted site.

5️⃣ Part 5 – Website Preview Pages (Screenshots 19–21)

🖼️ 19. About Page ([images/19-static-website-about.png](images/19-static-website-about.png))

Screenshot of the ‘About, Education, and Experience’ section of the hosted static website, captured while scrolling.

🖼️ 20. Projects Page ([images/20-static-website-projects.png](images/20-static-website-projects.png))

Screenshot of the ‘Projects’ section of the hosted static website, captured during scrolling.

🖼️ 21. Certificates Page ([images/21-static-website-certificates.png](images/21-static-website-certificates.png))

Screenshot of the ‘Technical Skills, Soft Skills, and Certificates’ section of the hosted static website.

🎥 Demo Video  
- [Watch on GitHub](https://github.com/DEEPIKAKANNAN25/AWS_Project/blob/main/Project-Demo/VideoRecording.mp4)  
- [Watch on Google Drive](https://drive.google.com/file/d/1qhMxOXe_KAva_LvUzdyg6Ny6Woib5dQF/view?usp=sharing)


🌟 Benefits of Hosting on Amazon S3

 • Scalable: Handles high traffic automatically.

 • Secure: IAM and bucket policies for access control.

 • Serverless: No infrastructure management needed.

 • Cost-effective: Pay only for what you use.

 • Highly Available: 99.99% uptime.

📚 Conclusion

• By completing this project, I gained the following skills and experience: 

• Gained hands-on experience deploying a static website on AWS S3.
 
• Learned how to configure public access and bucket policies.

• Built a secure, scalable, and serverless portfolio site.

• Demonstrated AWS S3's value for lightweight web hosting, ideal for portfolios, resumes, documentation, and more.
