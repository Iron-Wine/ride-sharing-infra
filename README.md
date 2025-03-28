# ride-sharing-infra
Ride Sharing Application 
step 1. Create New Repository ride-sharing-infra.
Create Project Directory-Initialize Git-Create Terraform files
Define AWS Provider (provider.tf) AWS US-East-1.
Create AWS CodeCommit for CI/CD (main.tf) creates codecommit repository for storing source code
Set up AWS Amplify for Frontend (main.tf) creates AWS Amplify app linked to the CodeCommit repository
Create Cognito User Pool for Authentication (main.tf) sets up cognito authetication for users
Create API Gateway (main.tf) defines API Gateway for handling API requests
Create a Lambda Function for Ride Requests(main.tf) creates Lambda function to handle ride requests
Create a DynamoDB Table to store rides (main.tf) creates DynamoDB table to store ride details
Create IAM Role for Lambda (iam.tf)grants lambda permissions to execute
Initialize and Apply Terraform-this deploys all resources on AWS
Push Terraform code to Github
Automate Deployment with GitHub Actions-applies terraform code i push updates to Github



Enable AWS Cloudwatchlogs for API Gateway and Lambda----creates IAM role for lambda with logging permissions, attaches policy to allow Lambda to write to cloudwatch, deploys lambda function that logs all activities
Enable Cloudwatch Merics and Alarms----reiggers an alert if lambda errors exceed 5 in one minute, seends an email notification via SNS
Setup Autoscaling for Lambda and DynamoDB----Limits lambda to 50 concurent executions to prevent over use, Autoscales DynamoDB read capacity when usage exceeds 70%
Push Terraform code to GitHub
Adding CI/CD for Terraform Deployment on AWS
Create a GitHub Actions Workflow----runs every push to the main branch, initializes, validates and applies infrastructure changes
Commit and Push Changes to Github


ROLLBACK
