AWS S3 Bucket Create
Login to AWS Console    https://aws.amazon.com/console/
Go to search bar and type S3
Click Create bucket
Bucket name(unique, lowercase + no spaces)
Region is default
Uncheck "Block all public access"

Click Create bucket

Open Bucket and upload(index.html and style.css) files and then upload

Bucket Properties, scroll down and enable static website hosting and then save

Edit Bucket Permissions and Bucket policy 
Here is the code of policy 
**{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-aws-s3-static-site-ilsa/*"
    }
  ]
}
Save

Go to the Properties tab of your S3 bucket
Scroll down to static website hosting and find the Endpoint URL.
Copy the URL and open it in your browser.
Your static website should now be live and accessible to anyone on the internet.
