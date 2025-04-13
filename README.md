

# nextwork-web-project

This is a simple Java web application created primarily for deployment on an AWS EC2 instance. The main goal of this project was to get hands-on experience in:

- Setting up a Java web application on an EC2 instance
- Creating and managing a local Git repository
- Connecting and pushing the project to a remote GitHub repository

## 🛠️ Technologies Used

- Java (Amazon Corretto 8)
- Apache Tomcat (assumed for deployment)
- Apache Maven (build and dependency management)
- AWS EC2 (Amazon Linux)
- Git

## 📁 Project Structure


nextwork-web-project/
├── README.md
├── pom.xml
└── src
    └── main
        ├── resources
        └── webapp
            ├── WEB-INF
            │   └── web.xml
            └── index.jsp


- `index.jsp`: The main entry point of the web app.
- `web.xml`: Configuration file for the web application.
- `pom.xml`: Maven configuration file with project dependencies and build setup.

## 🚀 Deployment Steps (Summary)

1. **Create EC2 Instance**
   - Launch a new EC2 instance (Amazon Linux or Ubuntu).
   - Open necessary ports (e.g., 8080 for Tomcat) in the security group.

2. **Install Java (Amazon Corretto 8) and Apache Maven**
   ```bash
   sudo yum install java-1.8.0-amazon-corretto
   sudo yum install maven
  

3. **Install and Configure Tomcat**
   - Download and extract Apache Tomcat.
   - Deploy your WAR file or copy project files to Tomcat’s `webapps` directory.

4. **Clone or Push Repo**
   - If creating the repo locally and pushing:
     ```bash
     git init
     git remote add origin https://github.com/Kalukwo/nextwork-web-project.git
     git add .
     git commit -m "Initial commit"
     git push -u origin main
     ```
   - If cloning an existing repo:
     ```bash
     git clone https://github.com/YOUR-USERNAME/nextwork-web-project.git
     ```



## 📌 Notes

- This project is for learning and demonstration purposes.
- No business logic or advanced features are included.
- Primary focus was infrastructure and version control setup.


