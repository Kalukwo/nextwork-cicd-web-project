

# nextwork-web-project

This is a simple Java web application created primarily for deployment on an AWS EC2 instance. The project is part of a complete **CI/CD pipeline** that automates the build, test, and deployment processes using AWS services. Any changes pushed to the GitHub repository are automatically built and deployed to a production environment on EC2.

## 🎯 Project Objectives

- Set up a Java web application hosted on an EC2 instance.
- Integrate the application with a full CI/CD pipeline using AWS services.
- Automate code deployment to production via GitHub commits.
- Gain hands-on experience with AWS DevOps tools and infrastructure as code.

## 🧰 Technologies & AWS Services Used

- Java (Amazon Corretto 8)
- Apache Maven (build and dependency management)
- Apache Tomcat (for deployment)
- Git & GitHub (version control)
- **AWS CodePipeline** – Orchestrates the CI/CD workflow.
- **AWS CodeBuild** – Builds the project from source.
- **AWS CodeDeploy** – Deploys the built artifact to EC2.
- **AWS CodeArtifact** – Manages dependencies (e.g., Maven).
- **AWS S3** – Stores build artifacts.
- **AWS EC2** – Hosts the Java web application.
- **AWS CloudFormation** – Provisions infrastructure resources.
- **IAM & VPC** – Secure and manage resources and access.

## 📁 Project Structure

nextwork-web-project/
├── README.md
├── pom.xml
└── src
└── main
├── resources
└── webapp
├── WEB-INF
│ └── web.xml
└── index.jsp

markdown
Copy
Edit

- `index.jsp`: The main entry point of the web app.
- `web.xml`: Configuration file for the web application.
- `pom.xml`: Maven build file specifying project dependencies.

## 🚀 CI/CD Pipeline Overview

1. **Code Commit**
   - Push changes to the GitHub repository.
2. **CodePipeline Trigger**
   - AWS CodePipeline detects the change and triggers the pipeline.
3. **Build Phase**
   - CodeBuild compiles the Java project using `pom.xml`.
   - Artifacts are uploaded to an S3 bucket.
4. **Deployment Phase**
   - CodeDeploy deploys the build to the target EC2 instance.
   - EC2 instance is provisioned via CloudFormation and configured to serve the application.
5. **Production**
   - Changes are reflected live on the website hosted on EC2.

## 🖥️ Manual Deployment (Alternative Summary)

If manually deploying to EC2:

1. **Launch EC2 Instance**
   - Amazon Linux 2 or Ubuntu, with port 8080 open.

2. **Install Java and Maven**
   ```bash
   sudo yum install java-1.8.0-amazon-corretto
   sudo yum install maven
Install and Configure Tomcat

Download and extract Apache Tomcat.

Deploy your WAR file or copy the project files into webapps.

Clone or Push the GitHub Repo

Push existing code:

bash
Copy
Edit
git init
git remote add origin https://github.com/Kalukwo/nextwork-web-project.git
git add .
git commit -m "Initial commit"
git push -u origin main
Or clone:

bash
Copy
Edit
git clone https://github.com/Kalukwo/nextwork-web-project.git
📘 Project Documentation Repository
For full documentation, architecture diagrams, and pipeline visuals, visit the Project Documentation Repository.

(Update the link above with your actual documentation repo URL)

📌 Notes
This project is for learning and demonstration purposes only.

No business logic or database layer is included.

Primary focus is on cloud infrastructure, CI/CD automation, and DevOps practice.

