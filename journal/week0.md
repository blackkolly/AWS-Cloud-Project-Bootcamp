# Week 0 — Billing and Architecture
The following activities were done in Week 0 of this bootcamp:
# Recreate Logical Architectural Diagram in Lucid Charts
Architecture diagrams are a great way to communicate your design, deployment, and topology. Examples of tools used for architecture diagrams are draw.io, hava.io, cloudockit, lucidchart, etc.
The Lucidchart was used in this bootcamp. Log in to lucid.app and create a free account. Then log in and start making use of the tools to create your architecture diagram.

# Create an Admin User
-	I clicked on “My Account” and chose the “AWS Management Console” from the drop-down menu. After signing in with my root user and password then I typed “IAM” in the search bar and select the suggested result.
-	It displayed the Identity and Access Management (IAM) dashboard and then click the “users” button on the left-hand pane.
-	Then on the succeeding page click the “Add users” button. And enter the desired name you will like to use.
-	In the navigation pane, choose Users, and then choose Add user.
-	In the User name box, enter a user name.
-	Choose both Programmatic access and AWS Management Console access.
-	Choose Next: Permissions.
-	Select the “Attach existing policies directly” and check the “Administrator Access” Click review and ensure the details are as desired and hit the “create user” button on the preceding page.
-	After creating the user please “download .csv file” and save it on your local machine or keep it securely in some folder.
-	Save the “Access key ID” and “Secret access key” in a text file and keep it securely for future reference.
# Use CloudShell
-	In this step, I launched AWS CloudShell from the console interface, choose an available AWS Region, and switch to your preferred shell, such as Bash, PowerShell, or   Z shell.

-	 From the AWS Management Console, you can also launch AWS CloudShell by choosing the AWS CloudShell icon.

# Generate AWS Credentials
Please move to "How to Create an Admin User" and follow the procedure to know how to generate an AWS credential.

# How to Installed AWS CLI
Download and run the AWS CLI MSI installer for Windows (64-bit):

https://awscli.amazonaws.com/AWSCLIV2.msi

To confirm the installation, open the Start menu, search for cmd or window PowerShell to open a command prompt window, and at the command prompt, use the aws --version command.

C:\> aws --version

# To configure the AWS CLI

I opened window PowerShell and input the below command from my aws credentials:

$ aws configure 
AWS Access Key ID : “xxxxxxxxxxxxxxx”
AWS Secret Access Key [None]: “xxxxxxxxxxxxxxx”
 Default region name [None]: “xxxxxxxx”
Default output format [None]: json

# Create a Billing Alarm
-	Sign in to the AWS Management Console.
-	Click the name of the account name on right hand bar and click the drop down menu and click Account or open the AWS Cost Management console.
-	In the left navigation panel, select Billing Preferences and, input the email address to get the alert notification and check the Receive Billing Alerts feature       settings. 
-	On the search bar type Cloud watch and click it. Navigate to CloudWatch dashboard 
-	In the left navigation panel, click Alarms to access the CloudWatch alarms available in the current AWS region.
-	Click create  alarm and select alarm metric then click billing and select Total estimated charge and tick USD .Then click select metric and select static under         threshold type  and click Greater under alarm condition. Define the threshold by input your value and click next. You can select the existing SNS topic or create a     new one and add notification email address. Then click next and input alarm name and click next and click create 
# Create a Budget
- Sign in to the AWS Management Console and open the AWS Cost Management console 
- In the navigation pane, I chose Budgets.
- At the top of the page, I chose Create budget.
- Under Budget setup, I chose Customize (advanced).
- Under Budget types, I choose Cost budget. Then, choose next.
- I input Budget name which must be a unique. It can contain A-Z, a-z, spaces, and special characters
- I chose monthly for every month I want the budget to reset the actual and forecasted spend.
- For Budget renewal I chose Recurring budget for a budget that resets after the budget period. 
- I chose the start date or period to begin tracking against budgeted amount. 
- For Budgeting method, selected Fixed but you can select the way that you want your budget   amount to be determined each budget period:
- I set budgeted amount to $10 to monitor every budget period.
- Then click next and create.

