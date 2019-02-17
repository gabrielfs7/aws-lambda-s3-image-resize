# aws-lambda-s3-image-resize

Simple code for AWS Lambda to process images resize using NodeJS and AWS S3 trigger.

# Requirements

- Have an **AWS account**.
- Have **NodeJS 8** installed locally to generate the node_modules.

# AWS configuration

1. Create **2 buckets** where one must have the sufix "resized", cause it will receive the resized images. I.e.

 - my-image-bucket
 - my-image-bucket-resized

2. Create a Lambda function and give the access role containing **AmazonS3FullAccess**. 

It will allow Lambda to read and write to your buckets.

3. Add an S3 trigger to your Lambda.

- Point it to your bucket **my-image-bucket**.
- The `Event type` must be **ObjectCreated**.

# How to use

Locally you need to generate the package that will be uploaded to aws. So in this project root folder:

1. Install the **node_modules**:

```
npm install
```

2. Generate a .zip file with containing the following files inside:

- index.js
- node_modules/


3. Updalod the .zip file through your AWS Lambda panel and publish a new version.

4. Upload some image to your not resized bucket (i.e: images).

5. The image resized will appear inside the **images-resized** bucket in a folder **resized-images**.