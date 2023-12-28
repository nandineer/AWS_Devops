
![image](https://github.com/nandineer/AWS_Devops/assets/22636122/f1ab1664-8701-4347-89de-90319303941b)



**Create a CI/CD Pipeline**
•	Navigate to CodeStar.
•	Click Create project.
•	If the Create service role dialog appears, click Create service role.
•	Click the HTML card.
•	Click Services and open EC2 in a new tab.
•	Click KeyPairs located in the navigation menu.
•	Click Create key pair.
•	For Name, enter pipeline.
•	Click Create key pair.
•	Back in the CodeStar browser tab, close the key pair dialog.
•	Click Next.
•	For Project name, enter Pipeline.
•	For the repository, select AWS CodeCommit.
•	For the Instance type, select t2.micro.
•	Choose the Subnet for us-east-1a.
•	Choose the pipeline and click ** Next**.
•	Click Create Project. It could take 5-10 minutes for the project to finish being set up.

**Deploy a New Version of a Website using a CI/CD Pipeline **

•	Click View application to navigate to our web application.
•	Back in the CodeStar browser tab, click IDE.
•	Click Access your project code.
•	Click Edit in AWS CodeCommit. This opens our repositories.
•	Click the webpage folder.
•	Click the index.html file. This is the code used to generate the website we just visited.
•	Click Edit.
•	Scroll down to line 61.
•	Change the h1 header in line 61 to:
•	Hello Cloud Gurus!
•	Change the h2 header in line 62 to:
•	You just deployed using your own CI/CD pipeline!
•	In the Commit changes to master section, set the following values:
o	Author name: Your name
o	Email address: test@test.com
o	Commit message: Update the website.
•	Click Commit changes.
•	In the CodeStar browser tab, click Pipeline to watch it all be deployed.
•	Refresh the web app we visited before, where we should see our new message we just edited in the code.
