
![image](https://github.com/nandineer/AWS_Devops/assets/22636122/e105b346-d3b0-486d-a649-0103cc07005e)




Create a CodeCommit Repository from the Management Console

•	Navigate to CodeCommit.
•	Under Repositories, click Create repository.
•	In Repository name, enter "sample-static-site".
•	Under Tags, click Add.
•	Set the following values:
o	Key: CreatedBy
o	Value: Your name
•	Click Create.
•	Add an index.html and JPG File to the Repository
•	Scroll to the bottom of the page and click Add file > Upload file.
•	Click Choose file and select the index.html file downloaded from GitHub.
•	In Commit changes to master, set the following values:
•	Author name: Your name
•	Email address: Your email
•	Commit message: Landing page
•	Click Commit changes.
•	Click Repositories.
•	Click sample-static-site to open the repository page.
•	Click Add file > Upload file.
•	Click Choose file and select the Mount.jpg file downloaded from GitHub.
•	In the Commit changes to master section, set the following values:
o	Author name: Your name
o	Email address: Your email
o	Commit message
•	Click Commit changes.
•	
Create an S3 Bucket and Configure It To Host a Static Website

•	Create an S3 Bucket
•	Navigate to S3.
•	Click Create bucket.
•	Set the following values:
•	Bucket name: Unique bucket name
•	Region: US East (N. Virginia)
•	Click Next > Next.
•	Deselect Block all public access.
•	Select I acknowledge that the current settings might result in this bucket and the objects within becoming public.
•	Click Add tag.
•	Set the following values:
o	Key: CreatedBy
o	Value: Your name
•	Leave the rest as their defaults and click Create bucket.
•	Enable Static Website Hosting
•	Click the newly created bucket to open it and select the Properties tab.
•	Scroll to Static website hosting at the bottom and click Edit.
•	In Static website hosting, select Enable.
•	Set the following values:
•	Index document: Index.html
•	Error document: error.html
•	Click Save changes.
•	Create an S3 Bucket Policy
•	Select the Permissions tab.
•	Scroll down to Bucket policy and click Edit.
•	Copy the bucket ARN number above the policy editor.
•	Click Policy Generator.
•	In Select Type of Policy, select S3 Bucket Policy.
•	In Add Statement(s), set the following values:
o	Effect: Allow
o	Principal: *
o	AWS Service: Amazon S3
o	Actions: GetObject
o	Amazon Resource Name (ARN): <BUCKET_ARN_NUMBER>/*
•	Click Add Statement.
•	Click Generate Policy.
•	Copy the generated policy to your clipboard.
•	Return to the bucket policy editor in S3 and paste in the policy.
•	Click Save changes.
•	
Create a Pipeline in AWS CodePipeline That Deploys a Static Website

•	Navigate to CodePipeline.
•	Under Pipelines click Create pipeline.
•	In Pipeline name, enter "sample-static-site-pipeline" and click Next.
•	On the Source page, set the following values:
•	Source provider: AWS CodeCommit
•	Repository name: sample-static-site
•	Branch name: main
•	In Change detection options, select AWS CodePipeline and click Next.
•	Click Skip build stage > Skip.
•	In Deploy on the next page, select Amazon S3 as the deploy provider.
•	Set the following values:
•	Region: US East (N. Virginia)
•	Bucket: Your bucket name
•	Click Extract file before deploy.
•	Leave the rest as their defaults and click Next.
•	Click Create pipeline.
•	Once the deploy stage completes, click the Amazon S3 URL under Deploy to verify deployment.
•	Select the Properties tab and scroll down to Static website hosting at the bottom of the page.
•	Click the bucket website endpoint URL to view the static website.
