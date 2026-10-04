:# 🚀 Jenkins CI/CD Pipeline with Docker

A complete CI/CD implementation using Jenkins, GitHub, Node.js, and Docker to automatically build, test, containerize, and deploy a web application.

---

## 📌 Project Overview

This project demonstrates the implementation of a Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins.

The pipeline connects a GitHub repository with Jenkins and automates the following process:

Developer
↓
GitHub Repository
↓
Jenkins
↓
Checkout Source Code
↓
Install Dependencies
↓
Run Tests
↓
Build Docker Image
↓
Deploy Docker Container
↓
Running Application

The application is a simple Node.js web application that is packaged into a Docker container and deployed through Jenkins.

---

## 🎯 Objective

The main objectives of this project are:

- Understand Jenkins CI/CD fundamentals
- Integrate Jenkins with GitHub
- Create and configure a Jenkins Pipeline
- Automate application dependency installation
- Automate application testing
- Build a Docker image
- Deploy the application using Docker
- Understand CI/CD workflow
- Verify successful application deployment

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Jenkins | CI/CD automation |
| GitHub | Source code management |
| Git | Version control |
| Node.js | Application runtime |
| Express.js | Web application framework |
| Docker | Application containerization |
| Linux/Ubuntu | Jenkins server environment |

---

# 📂 Project Structure

```text
devops-task-2-jenkins/
│
├── Dockerfile
├── Jenkinsfile
├── package.json
├── package-lock.json
├── server.js
├── README.md
│
└── Screenshots/
    ├── Screenshot_2026-10-04-13-29-16-03_e5d3893ac03954c6bb675ef2555b879b.jpg
    ├── Screenshot_2026-10-04-13-29-21-....jpg
    ├── Screenshot_2026-10-04-13-29-34-....jpg
    ├── Screenshot_2026-10-04-13-29-....jpg
    └── Screenshot_2026-10-04-....jpg
🏗️ Application Architecture
                 ┌─────────────────────┐
                 │      Developer      │
                 └──────────┬──────────┘
                            │
                         git push
                            │
                            ▼
                 ┌─────────────────────┐
                 │       GitHub        │
                 │   Source Repository │
                 └──────────┬──────────┘
                            │
                       Webhook/Trigger
                            │
                            ▼
                 ┌─────────────────────┐
                 │       Jenkins       │
                 │    CI/CD Server     │
                 └──────────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
          Checkout        Build/Test    Docker Build
              │             │             │
              └─────────────┼─────────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Docker Container  │
                 │    Node.js App      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │    Web Browser      │
                 └─────────────────────┘
🔄 CI/CD Workflow
1. Developer Push

The developer makes changes to the application and pushes the updated code to the GitHub repository.

2. GitHub Repository

GitHub stores and manages the application source code and Jenkins configuration.

3. Jenkins Checkout

Jenkins retrieves the latest source code from the GitHub repository.

4. Build

Jenkins installs the required Node.js dependencies.

npm install
5. Test

Jenkins executes the configured application tests.

npm test
6. Docker Build

Jenkins builds a Docker image using the Dockerfile.

docker build -t devops-task-2-jenkins .
7. Deploy

Jenkins runs the Docker container using the generated image.

docker run -d -p 3000:3000 devops-task-2-jenkins
8. Application Verification

The deployed application can be verified through the browser.

🧩 Jenkins Pipeline Stages

The Jenkinsfile contains the CI/CD pipeline stages.

Stage 1 — Checkout

Retrieves the source code from GitHub.

Purpose

This stage ensures that Jenkins works with the latest version of the application source code.

Stage 2 — Build

Installs the required Node.js dependencies.

npm install
Purpose

Downloads and installs the packages required by the application.

Stage 3 — Test

Runs the application tests.

npm test
Purpose

Testing helps verify that the application is working correctly before deployment.

Stage 4 — Docker Build

Creates the Docker image.

docker build -t devops-task-2-jenkins .
Purpose

Packages the application and its dependencies into a portable Docker image.

Stage 5 — Deploy

Runs the application inside a Docker container.

docker run -d -p 3000:3000 devops-task-2-jenkins
Purpose

Deploys the latest application version using Docker.

📝 Jenkinsfile

The project uses a Jenkins Pipeline to automate the complete CI/CD process.

The pipeline performs:

Checkout
   ↓
Build
   ↓
Test
   ↓
Docker Build
   ↓
Deploy
   ↓
Application Running

The Jenkinsfile is stored in the GitHub repository along with the application source code.

🐳 Docker Configuration

Docker is used to containerize the Node.js application.

Dockerfile

The Dockerfile defines the environment required to run the application.

Example:

FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]
Dockerfile Explanation
Instruction	Purpose
FROM node:18	Uses Node.js base image
WORKDIR /app	Sets application working directory
COPY package*.json ./	Copies package files
RUN npm install	Installs dependencies
COPY . .	Copies application source code
EXPOSE 3000	Exposes application port
CMD	Starts the application
🌐 Application

The Node.js application runs inside the Docker container.

The application is exposed through port:

3000

The application can be accessed using:

http://localhost:3000

or through the server public IP when deployed on a cloud server.

🧪 Testing

The application is tested as part of the Jenkins pipeline.

The testing stage ensures that the application works correctly before Docker deployment.

Example command:

npm test

If the test stage is successful, Jenkins continues to the Docker build and deployment stages.

If the test stage fails, the pipeline stops and the deployment is not performed.

🔗 GitHub Integration

The project source code is maintained in GitHub.

GitHub is used for:

Source code management
Version control
Jenkins integration
Storing Jenkinsfile
Storing Docker configuration
Project documentation

Repository:

https://github.com/sindhupriya5e1/devops-task-2-jenkins

⚙️ Jenkins Integration

Jenkins is configured to retrieve the source code from GitHub and execute the pipeline.

The Jenkins pipeline performs:

GitHub Repository
       ↓
Jenkins
       ↓
Checkout
       ↓
Build
       ↓
Test
       ↓
Docker Build
       ↓
Deploy
       ↓
Success
🐳 Docker Deployment Verification

The Docker container can be verified using:

docker ps

The running container should display the application port mapping:

3000:3000

Docker images can be checked using:

docker images
📸 Project Screenshots
1. GitHub Repository

This screenshot shows the GitHub repository containing the project files, Jenkinsfile, Docker configuration, application files, and README.

2. Jenkins Pipeline

This screenshot demonstrates the Jenkins pipeline execution.

The pipeline stages are executed in sequence:

Checkout
   ↓
Build
   ↓
Test
   ↓
Docker Build
   ↓
Deploy

3. Jenkins Console Output

The Jenkins console output demonstrates the actual execution of the CI/CD pipeline.

It verifies:

Source code checkout
Dependency installation
Testing
Docker image creation
Docker deployment
Successful pipeline completion

4. Docker Container

This screenshot shows the Docker container created during the deployment process.

The application is running inside the Docker container and is exposed through port 3000.

5. Application Output

This screenshot shows the final application output after successful deployment.

📊 CI/CD Result

The completed pipeline successfully demonstrates:

Component	Result
GitHub Integration	✅ Successful
Jenkins Checkout	✅ Successful
Dependency Installation	✅ Successful
Application Testing	✅ Successful
Docker Image Build	✅ Successful
Docker Container Deployment	✅ Successful
Application Verification	✅ Successful
CI/CD Pipeline	✅ Completed
🔐 Security Considerations

For a production environment:

Do not commit passwords or API tokens to GitHub.
Do not expose Jenkins credentials.
Use Jenkins Credentials Manager.
Use GitHub Secrets for sensitive information.
Configure proper firewall/security-group rules.
Use HTTPS for production applications.
Keep Jenkins, Docker, Node.js, and dependencies updated.
📚 Key DevOps Concepts Demonstrated
Continuous Integration

Continuous Integration automatically builds and tests application changes.

Benefits:

Early bug detection
Automated testing
Faster feedback
Better code quality
Continuous Deployment

Continuous Deployment automatically deploys successfully tested application changes.

In this project:

Code Change
    ↓
GitHub
    ↓
Jenkins
    ↓
Build
    ↓
Test
    ↓
Docker Build
    ↓
Deployment
Jenkins

Jenkins is an automation server used to implement CI/CD pipelines.

In this project Jenkins performs:

Source Checkout
Dependency Installation
Testing
Docker Build
Deployment
Docker

Docker packages the application and its runtime dependencies into a container.

This provides a consistent environment for running the application.

Jenkinsfile

The Jenkinsfile defines the CI/CD pipeline as code.

Advantages:

Version controlled
Reproducible
Easy to maintain
Stored together with source code
💡 Why CI/CD Is Important

Without CI/CD:

Developer
   ↓
Manual Build
   ↓
Manual Testing
   ↓
Manual Deployment

With CI/CD:

Developer
   ↓
Git Push
   ↓
Jenkins
   ↓
Automated Build
   ↓
Automated Test
   ↓
Docker Build
   ↓
Deployment

CI/CD reduces repetitive manual work and makes software delivery faster and more reliable.

🎓 Learning Outcomes

Through this project, I gained practical experience with:

Jenkins Pipeline creation
Jenkinsfile configuration
GitHub integration
CI/CD automation
Docker image creation
Docker container deployment
Node.js application deployment
Automated testing
Linux/Cloud environment
Pipeline troubleshooting
DevOps workflow
✅ Conclusion

This project successfully demonstrates a complete CI/CD pipeline using Jenkins, GitHub, Node.js, and Docker.

The application source code is maintained in GitHub, Jenkins automates the build and testing process, Docker containerizes the application, and the final application is deployed through the CI/CD pipeline.

The project provides practical understanding of DevOps automation and the complete software delivery lifecycle.

👨‍💻 Project Status

Status: ✅ Successfully Completed

Technologies: Jenkins | GitHub | Node.js | Docker | CI/CD
