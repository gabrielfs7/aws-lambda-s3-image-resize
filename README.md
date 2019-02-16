# aws-lambda-s3-image-resize

Simple code to process image resize using NodeJS, AWS S3 and Lambda


# Requirements

- Have an **AWS account**.
- Have **NodeJS 8** installed locally to generate the node_modules.
- Create **2 buckets** (one must have the sufix "resized"). I.e: "images" and "images-resized".
- Give **AmazonS3FullAccess** role to your Lambda function.

# How to use

1. Install the **node_modules**:

```
npm install
```

2. Generate a .zip file with containing the following files inside:

- index.js
- node_modules/


3. Updalod the .zip file through your AWS Lambda panel.

4. Upload some image to your not resized bucket (i.e: images).

5. The image resized will appear inside the **images-resized** bucket in a folder **resized-images**.