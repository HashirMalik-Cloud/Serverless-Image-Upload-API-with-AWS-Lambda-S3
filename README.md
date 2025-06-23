# Serverless-Image-Upload-API-with-AWS-Lambda-S3
A simple serverless image uploader using AWS Lambda, API Gateway, and S3. It accepts base64 images via HTTP POST and stores them in S3 with unique names. Ideal for learning or lightweight apps. 📄 Full explanation, code breakdown &amp; screenshots are in the attached Project Notes.


Photo Upload API using AWS Lambda + API Gateway + S3
This project is a serverless image uploader built with AWS.
Users can send a base64-encoded image via HTTP POST request, and it automatically gets saved in an S3 bucket.
________________________________________
✅ What This Project Does
•	Accepts base64 image data through an HTTP API (Postman)
•	Uses a Lambda function to decode the image
•	Saves it in Amazon S3 with a unique file name
•	Sends back a success response
No servers, no backend to manage — 100% serverless.
________________________________________
🛠️ Tools & Services Used
•	AWS Lambda
•	API Gateway
•	Amazon S3
•	IAM (for permissions)
•	Postman (to test API)
•	Python (boto3)
________________________________________
🔧 Steps I Followed
1.	Created an S3 bucket
o	For storing uploaded images

2.	Wrote a Lambda function (Python)
o	Decodes the image from base64
o	Saves it to S3 with a unique UUID filename

 
3.	Attached permissions to Lambda
o	Gave it rights to PutObject in my S3 bucket
 



4.	Created an API Gateway (HTTP API)
o	Connected it to my Lambda function
o	Got a public endpoint to receive POST requests
 

5.	Tested the API using Postman
o	Sent base64-encoded images
o	Confirmed successful uploads to S3
 

6.	Got success responses and verified in S3

 



________________________________________
📌 Notes
•	Images are named using UUIDs (no duplicates)
•	The Lambda function is lightweight and cost-effective
•	Can be extended easily to add auth, metadata, or DynamoDB

