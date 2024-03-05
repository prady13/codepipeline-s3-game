Step 1: create a S3 bucket which will pull the code of the website from the repo and allow public access
<img width="1440" alt="Screenshot 2024-03-05 at 8 19 56 PM" src="https://github.com/prady13/codepipeline-s3-game/assets/62207613/bb7d1b7a-efd9-45a7-9d59-bdafbd1607d9">

Step 2: Enable static website hosting in the S3 bucket.
Step 3: Add the bucket policy to allow everybody to read all files on our bucket.
{
    "Version": "2012-10-17",
    "Statement": [
    	{
        	"Sid": "PublicReadGetObject",
        	"Effect": "Allow",
        	"Principal": "*",
        	"Action": [
            	"s3:GetObject"
        	],
        	"Resource": [
                "arn:aws:s3:::my-meme-game-prady/*"
        	]
    	}
    ]
}

