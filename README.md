# node-todo-cicd

**Introduction:**

This guide is about configuring freestyle CI/CD Node JS projects with Jenkins using GitHub Webhooks. This README explains step-by-step instructions from cloning the repository to configuring webhooks and deployments, ensuring flawless and automated development work. 

**Pre-requisites:**

Create an EC2 instance as Jenkins Server for this project and install the following applications over there:
1. Install Jenkins
2. Install Java
3. Install Docker and Docker Compose

**Setting up Jenkins server:**

1. With the help of Jenkins server IP address, log in to Jenkins through a web browser and access Jenkins Dashboard.
2. Create a new Jenkins job for your project:-

   2.1 Choose 'New Item' from the dashboard.
   
   2.2 Provide a name for your job and select the appropriate project type according to your requirement.

   2.3 Configure the source code management settings using Git.

4. Install necessary plugins to enable GitHub integration and Docker support, based on your project's requirements.

**Configuring GitHub Webhooks:**

1. Log in to your GitHub account repository, and navigate to repository 'Settings' > 'Webhooks'.
2. Click 'Add webhook':

   2.1. Enter the Payload URL, which should be your Jenkins job's URL followed by '/gitHub-webhook/'.

   2.2. Choose the content type as 'application/JSON'.

   2.3 Select the events that should trigger the webhook (e.g., 'Push events').  

3. Save the webhook configuration and refresh the page.

**Deploy your code:**

1. Configure your Jenkins job:

   -Specify the GitHub repository URL.

   -Set up build triggers to use the GitHub webhook.

2. Set up deployment steps in the Jenkins job:

   -Based on your project requirement, use Docker Compose, scripts, or other tools.

   -Ensure that the builds are triggered and deployed  application successfully.

3. Whenever code changes are pushed to your GitHub repository, the webhook will trigger the Jenkins job automatically.

**Troubleshooting**:

Considering the pre-requisites of this project you may face the other following issues while deploying this Project:

1. Check Groovy syntax while writing the build script.
2. Open mentioned port in the inbound rules of the EC2 instance.
3. Make sure mentioned port is free, and not used by other applications.
4. If you encounter other errors, Google it and try to understand what mistake have you done also don't hesitate to ask with TWS community.

!!!!!-----------------------------------------------------------------------------------------------------------------------------------------------!!!!





