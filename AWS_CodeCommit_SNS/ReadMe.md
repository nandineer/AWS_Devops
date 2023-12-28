
![image](https://github.com/nandineer/AWS_Devops/assets/22636122/2d830c0f-45a4-429f-a32f-ca1bdbe533d2)



**Create a CodeCommit Repository**
  1.	Open the CodeCommit console.
  2.	On the Repositories page, click Create repository.
  3.	On the Create repository page, set the following values:
  •	Repository name: codecommitnotifications
  •	Description: Leave as default.
  1.	Click Create.
**Create an Amazon SNS topic**
  1.	Navigate to Amazon SNS.
  2.	On the homepage, enter the topic name CodeCommitNotify in the Create Topic section.
  3.	Click Next step.
  4.	On the Create topic page, select the Standard option and leave everything else as the default.
  5.	Click Create topic.
**Subscribe to the Topic**
  1.	From the CodeCommitNotify page, click Create subscription.
  2.	On the Create subscriptions page, set the following values:
    o	Protocol: Email
    o	Endpoint: Enter your email address.
  3.	Click Create subscription to send a confirmation message to the registered email.
  4.	Open the AWS Subscription Confirmation email and click Confirm subscription.
  5.	Return to the Amazon SNS page and check that the confirmation went through.
**Create an Event**
  1.	Navigate to EventBridge.
  2.	On the landing page, under Get Started on the right side of the page, ensure EventBridge Rule is selected and click Create Rule.
  3.	On the Create rule page, set the following values:
    o	Name: codecommitrule
    o	Event bus:default
  4.	Select Rule with an event pattern
  5.	Click Next.
  6.	In Event source, select AWS events or EventBridge partner events.
  7.	In the Event Pattern section, choose the Event source of AWS Services.
  8.	Choose the CodeCommit service.
  9.	Choose the event type of All Events.
  10.	Click Next.
  11.	Choose the Target type of AWS service.
  12.	Select a target of SNS topic.
  13.	Choose your Topic name.
  14.	Click Next.
  15.	Click Next.
  16.	Click Create rule.
**Add a File to the Repository**
  1.	Navigate back to CodeCommit.
  2.	On the Repositories page, select the newly created repository.
  3.	Click Add file > Upload file.
  4.	Upload a file from your local computer.
  5.	In the Commit changes to master section, set the following values:
    o	Author name: Enter your name.
    o	Email address: Enter your email address.
    o	Commit message: Select Added file..
  6.	Click Commit changes.
  7.	Check your email to see if you received a notification of a change to the repository.

