# CI/CD Pipeline Automation using Jenkins, Docker & GitHub

## 📌 Project Overview

This project demonstrates a complete **CI/CD (Continuous Integration and Continuous Deployment) pipeline** using **GitHub, Jenkins, Docker, and Node.js**.

The main objective of this project is to automate the process of taking application source code from a GitHub repository, building and testing it through Jenkins, creating a Docker image, and running the application inside a Docker container.

The complete workflow is:

**Developer → GitHub → Jenkins → Build → Test → Docker Build → Docker Run → Successful Deployment**

---

## 🛠️ Technologies Used

* **GitHub** – Source code repository
* **Jenkins** – CI/CD automation server
* **Docker** – Containerization
* **Node.js** – Application runtime
* **Git** – Version control
* **GitHub Webhook / Pipeline** – Automated triggering
* **Jenkins Pipeline** – Build automation

---

# 1. Project Source Code

The project source code is maintained in a GitHub repository.

GitHub is used to store the application files, Dockerfile, package.json, server.js and Jenkins pipeline configuration.

### Project Repository

GitHub Repository:

`https://github.com/sindhupriya5e1/nodejs-demo-app`

The repository contains the required files for building and running the Node.js application.

---

# 2. Node.js Application

The application is created using Node.js.

The main application file is:

`server.js`

The application starts a Node.js server and provides a simple response when the application is accessed.

The `package.json` file contains the project information and required dependencies.

---

# 3. Dockerfile

A Dockerfile is created to containerize the Node.js application.

The Dockerfile defines:

* Base Node.js image
* Working directory
* Application dependencies
* Source code
* Application port
* Command to start the application

Docker allows the application to run consistently in an isolated container environment.

---

# 4. Docker Image Creation

After creating the Dockerfile, a Docker image is built using the application source code.

The Docker image contains everything required to run the application, including:

* Node.js environment
* Application source code
* Dependencies
* Runtime configuration

The image can then be used to create a running Docker container.

---

# 5. Jenkins Setup

Jenkins is used as the CI/CD automation tool.

The Jenkins server is configured to connect with the GitHub repository.

A Jenkins Pipeline Job is created for this project.

The pipeline automatically performs the required build and deployment steps.

---

# 6. Jenkins Pipeline Configuration

A Jenkins Pipeline is created to automate the complete workflow.

The pipeline contains multiple stages.

### Pipeline Stages

1. **Checkout**
2. **Install Dependencies**
3. **Build**
4. **Test**
5. **Docker Build**
6. **Docker Run / Deploy**

Each stage performs a specific task in the CI/CD process.

---

# 7. Checkout Stage

In the Checkout stage, Jenkins retrieves the latest source code from the GitHub repository.

This ensures that Jenkins always works with the latest available version of the project.

**GitHub → Jenkins**

---

# 8. Install Dependencies

After checking out the source code, Jenkins installs the Node.js project dependencies using:

`npm install`

This downloads and installs all dependencies defined in `package.json`.

---

# 9. Build Stage

The Build stage verifies that the application can be prepared successfully for execution.

Jenkins executes the required build commands and checks for build-related errors.

If the build is successful, Jenkins proceeds to the next stage.

---

# 10. Test Stage

The Test stage is used to verify the application.

Jenkins executes the configured test commands and checks whether the application passes the required validations.

If the tests are successful, the pipeline continues.

If a stage fails, Jenkins stops the pipeline and reports the failure.

---

# 11. Docker Build Stage

After the application build and test stages are completed successfully, Jenkins creates the Docker image.

The Docker image is created using the project's Dockerfile.

This converts the application into a portable container image.

The process is:

**Source Code → Dockerfile → Docker Image**

---

# 12. Docker Container

After successfully creating the Docker image, a Docker container is created from that image.

The container runs the Node.js application in an isolated environment.

The application can then be accessed through the configured port.

The process is:

**Docker Image → Docker Container → Running Application**

---

# 13. Jenkins Build Execution

The Jenkins job is executed after configuring the pipeline.

Jenkins performs all the configured stages automatically.

The build console provides detailed information about every step performed by Jenkins.

The console output helps verify:

* GitHub checkout
* Dependency installation
* Build execution
* Testing
* Docker image creation
* Container execution

---

# 14. Jenkins Pipeline Stages

The Jenkins Pipeline view displays all stages of the CI/CD process.

When every stage completes successfully, all stages are displayed as **green**.

Example:

**Checkout ✅ → Install Dependencies ✅ → Build ✅ → Test ✅ → Docker Build ✅ → Deploy ✅**

This confirms that the complete pipeline executed successfully.

---

# 15. Successful Build

After all stages are completed without errors, Jenkins marks the build as:

## ✅ SUCCESS

The Jenkins console output shows that the pipeline completed successfully.

This confirms that:

* Source code was retrieved successfully.
* Dependencies were installed successfully.
* Application build was successful.
* Tests were completed successfully.
* Docker image was created successfully.
* Docker container was started successfully.

---

# 16. Final Output

The final result of the project is a successfully automated CI/CD pipeline.

The application source code is maintained in GitHub, Jenkins automatically processes the project, Docker creates the application container, and the final application runs successfully.

### Complete Workflow

```text
GitHub Repository
       ↓
Jenkins Pipeline
       ↓
Checkout Source Code
       ↓
Install Dependencies
       ↓
Build Application
       ↓
Run Tests
       ↓
Build Docker Image
       ↓
Run Docker Container
       ↓
Application Running
       ↓
Jenkins Build SUCCESS ✅
```

---

# 17. Screenshots

The following screenshots are included as proof of the successful implementation:

### Screenshot 1 – GitHub Repository

Shows the project source code and repository files.

### Screenshot 2 – Jenkins Job / Build

Shows the Jenkins project and executed build.

### Screenshot 3 – Jenkins Console Output

Shows the complete console output with the final **SUCCESS** status.

### Screenshot 4 – Jenkins Pipeline Stages

Shows all pipeline stages completed successfully in green.

### Screenshot 5 – Jenkins Pipeline Steps

Shows the individual steps executed during the CI/CD process.

---

# 18. Conclusion

This project demonstrates how a simple Node.js application can be integrated with a complete CI/CD workflow using GitHub, Jenkins, and Docker.

The pipeline automates the major software delivery steps, reduces manual effort, and provides a repeatable process for building, testing, containerizing, and deploying an application.

The successful Jenkins build and green pipeline stages confirm that the CI/CD pipeline has been implemented and executed successfully.

## ✅ Final Status

**CI/CD Pipeline: SUCCESS**

**Application Build: SUCCESS**

**Docker Build: SUCCESS**

**Deployment: SUCCESS**
