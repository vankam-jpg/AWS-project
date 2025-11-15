Deploying static website on AWS

About the project:
 
 Project Overview
This project demonstrates how to deploy a static website using Amazon Web Services (AWS). The deployment uses Amazon S3, Amazon CloudFront. 
The goal of this project is to showcase knowledge of cloud deployment, versioning, security etc.
AWS Services Used
•	Amazon S3 – Host the website files (HTML, CSS, JS, images)
•	Amazon CloudFront – CDN distribution for faster content delivery
•	AWS IAM – Secure access and permissions
Project Structure:
bucket-name/
   index.html
   style.css
   script.js
   images/
Steps to deploy the project:
1.	Creating the S3 bucket
•	Go to AWS console  S3
•	Click create bucket
•	Create bucket with gobally unique name.
•	Enable the public acces to the bucket.
•	Click create bucket.
2.	Uploading website files in the bucket.
•	Click the upload button in the bucket.
•	Add all files and floders related to the website.
•	Make files public.
3.	Configure bucket policy
•	Click permissions tab.
•	In the bucket policy section click edit button.
•	Enter the code below and name name to your bucket name 
•	click save
	{
	  "Version":"2012-10-17",
	  "Statement":[
	    {
	      "Sid":"AddPerm",
	      "Effect":"Allow",
	      "Principal": "*",
	      "Action":["s3:GetObject"],
	      "Resource":["arn:aws:s3:::mybucket-3126-9063-3537/*"]
	    }
	  ]
	}
4.	Static website hosting and copy endpoint
•	Go to properties tab
•	In static website hosting section click edit.
•	Enable the static website hosting.
•	Enter index.html in the index document.
•	Save the changes and copy the website endpoint.
5.	Creating the distribution in the cloudFront.
•	Select cloudfront from the services 
•	In the dashboard click create distribution.
•	Follow all the steps and click create distribution.
6.	Attaching the S3 pages to the Distribution.
•	Once distribution created select it
•	Paste the end point in the distribution and  origin name.
•	Enable and deploy distribution.
Final output:
Your static website is successfully deployed!
You can access it using:
•	S3 Website URL:
http://mybucket-3126-9063-3536.s3-website-region.amazonaws.com
•	CloudFront URL:
d2i0buzs5vy6v.cloudfront.net

