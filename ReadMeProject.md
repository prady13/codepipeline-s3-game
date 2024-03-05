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

Step 3: Now we will create a new Pipeline that will orchestrate getting the code from github to the bucket.
<img width="1440" alt="Screenshot 2024-03-05 at 9 15 29 PM" src="https://github.com/prady13/codepipeline-s3-game/assets/62207613/7389b209-fa30-4e5a-97e3-517061f7cc9a">

Pipeline successfully connected
<img width="1440" alt="Screenshot 2024-03-05 at 9 21 55 PM" src="https://github.com/prady13/codepipeline-s3-game/assets/62207613/a038a184-0e78-408e-b610-b042edd68d77">

<img width="1440" alt="Screenshot 2024-03-05 at 9 25 57 PM" src="https://github.com/prady13/codepipeline-s3-game/assets/62207613/9a6423c9-7920-4ca6-9e98-9fb79037e494">

Now the pipeline is succesfully connected and we can access the live url from the bucket for our website.
![Uploading Screenshot 2024-03-05 at 9.27.04 PM.png…]()

