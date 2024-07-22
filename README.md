# ImageResizingAWS
This project automates image processing and management within the AWS ecosystem. It aims to streamline image handling by automatically resizing images and transferring them to a designated storage location, with notifications sent to stakeholders. Key AWS services used include Lambda, S3, and SNS to orchestrate this workflow.


**Image Processing Automation:** Automatically **resize and optimize** images upon upload.

**Secure Storage:** Store processed **images securely** and reliably in an S3 bucket.

**Real-time Notifications:** Receive **immediate updates** on image processing via SNS.

**Scalable Architecture:** Designed to **scale efficiently** to meet image processing demands.

**Cost-efficient Solution:** Utilize AWS **serverless** technologies to minimize operational costs.

![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/2044f073-08c3-4996-819d-98ace21fd690)

_Created TWO S3 Buckets_
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/fd637bd7-e4a3-445f-9932-49e8fa15b76f)

_Now we Make SNS Notification_
Notification will be sent on the Email by which we have subscribed to SNS.
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/c2807887-827b-4134-997f-60aaf6ff472b)

_Now we create LAMBDA functions_
We used the given PYTHON CODE.
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/f82d27f6-bc44-4abd-b889-0772ff9a66ed)

We give certain Permissions to our Lambda Function by attaching certain policies to it.
Also we added S3 bucket as a _**TRIGGER**_ for our Lambda Function.
We add python Pillow Library for Lambda Function (We can do it by Importing it in code but that is time consuming).
(arn:aws:lambda:ap-south-1:770693421928:layer:Klayers-p39-pillow:1) adding in layer SPECIFIC ARN.

Now in source bucket we are adding a .jpg File to resize
We are adding 2 images
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/ab9b9295-10f4-4581-b3df-05e26aeb7075)

In Resize Image Bucket we have our Resized Images
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/c6d4bc47-72f4-42ea-9fb1-b20636473fcb)

SNS Notification
![image](https://github.com/divyanshgoel09/ImageResizingAWS/assets/118998853/cd3cf831-f0fb-479e-9499-092d70ad9638)



