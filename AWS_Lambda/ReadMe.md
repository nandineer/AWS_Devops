![image](https://github.com/nandineer/AWS_Devops/assets/22636122/84dd36fe-93c8-4b06-803c-c1a51cc884b3)


**Create a Lambda Function within the AWS Lambda Console**

•	Navigate to Lambda.
•	Click Create a function.
•	Make sure the Author from scratch option at the top is selected, and then use the following settings:
  o	Basic information:
  o	Name: HelloWorld
  o	Runtime: Python3.7
  o	Permissions:
  o	Click on Change default execution role.
  o	Execution role: Use an existing role
  o	Existing role: lambdarole
•	Click Create function.
•	On the HelloWorld page, scroll to the Function code section.
•	Delete the existing code there, and enter the code from GitHub.
•	Click Deploy.
**Create a Test Event and Manually Invoke the Function Using the Test Event**

•	In the dropdown next to Test at the top of the Code Source section, select Configure test event.
•	In the dialog, select Create new event.
•	Give it an event name (e.g., "Test").
•	Select the Hello World event template.
•	Replace the current code there with the provided JSON code, and then click on Save.
•	Click Test to verify the function's success.

**Verify That CloudWatch Has Captured Function Logs**

•	Navigate to CloudWatch.
•	Select Logs and then Log groups in the left-hand menu.
•	Click on the log group with your function name in it.
•	Click on the log stream within the log group.
•	Verify the output is present and correct.
