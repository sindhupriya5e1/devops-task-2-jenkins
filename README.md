# Task 2 – Jenkins CI/CD Pipeline

## 1. Project Overview

This project demonstrates a **CI/CD pipeline using Jenkins** to automate the process of building, testing, and deploying a Node.js application.

The main objective of this task is to understand how Jenkins can automate the software delivery process whenever new code is pushed to a GitHub repository.

The complete workflow is:

**Developer → GitHub → Jenkins → Build → Test → Pipeline Stages → Successful Build**

---

## 2. Objective

The objectives of this project are:

* To configure Jenkins for CI/CD automation.
* To connect Jenkins with a GitHub repository.
* To automatically fetch source code from GitHub.
* To install project dependencies.
* To build and test the application.
* To execute the pipeline using a Jenkinsfile.
* To monitor pipeline stages and build status.
* To verify the successful execution of the CI/CD pipeline.

---

## 3. Technologies Used

* **GitHub** – Source code repository
* **Jenkins** – CI/CD automation server
* **Node.js** – Application runtime
* **npm** – Package and dependency management
* **Git** – Version control
* **Jenkinsfile** – Pipeline configuration

---

## 4. Project Structure

The project contains the application source code along with the Jenkins pipeline configuration.

```text
nodejs-demo-app/
│
├── server.js
├── package.json
├── Jenkinsfile
└── README.md
```

### Important Files

**server.js**
Contains the Node.js application code.

**package.json**
Contains project information, dependencies, and scripts required to run the application.

**Jenkinsfile**
Defines the complete CI/CD pipeline stages that Jenkins executes automatically.

**README.md**
Contains the project documentation, setup procedure, pipeline explanation, and screenshots.

---

# 5. Step-by-Step Project Workflow

## Step 1 – Create the GitHub Repository

First, the Node.js application project was created and pushed to a GitHub repository.

The repository contains the application source code and the Jenkinsfile required for CI/CD automation.

GitHub acts as the central source-code repository where the project files are maintained.

---

## Step 2 – Create the Node.js Application

A simple Node.js application was used for this project.

The application contains the required source code and `package.json` file.

The application can be executed using Node.js after installing the required dependencies.

---

## Step 3 – Create the Jenkinsfile

A `Jenkinsfile` was added to the project repository.

The Jenkinsfile defines the stages that Jenkins should execute during the CI/CD process.

The pipeline is divided into multiple stages such as:

1. Checkout
2. Install Dependencies
3. Build
4. Test
5. Final Verification

Example pipeline flow:

```text
Checkout
   ↓
Install Dependencies
   ↓
Build
   ↓
Test
   ↓
Pipeline Success
```

---

# 6. Jenkins Configuration

## Step 4 – Open Jenkins

Jenkins was opened and the Jenkins dashboard was accessed.

A new Jenkins Pipeline job was created for the project.

---

## Step 5 – Create Jenkins Pipeline Job

A new Jenkins job was created by selecting the **Pipeline** project type.

The job was configured to use the project's Jenkinsfile from the GitHub repository.

The GitHub repository URL was provided in the Jenkins configuration.

---

## Step 6 – Connect GitHub Repository

Jenkins was connected to the GitHub repository so that it could access the project source code.

The repository contains the Jenkinsfile, which tells Jenkins how to execute the CI/CD pipeline.

---

# 7. Pipeline Execution

## Step 7 – Run the Jenkins Pipeline

After configuring the Jenkins job, the pipeline was executed using **Build Now**.

Jenkins then started executing the stages defined in the Jenkinsfile.

The pipeline automatically performed the required steps without manually executing each command.

---

## Step 8 – Checkout Stage

In the first stage, Jenkins checked out the source code from the GitHub repository.

This allows Jenkins to work with the latest version of the application code.

```text
GitHub Repository
       ↓
Jenkins
       ↓
Source Code Checkout
```

---

## Step 9 – Install Dependencies

Jenkins installed the Node.js project dependencies using npm.

The dependencies defined in `package.json` were installed so that the application could be built and tested.

---

## Step 10 – Build Stage

The build stage verifies that the application can be prepared successfully without errors.

Jenkins executes the configured build commands from the pipeline.

If the build is successful, Jenkins proceeds to the next stage.

---

## Step 11 – Test Stage

The testing stage verifies the application and ensures that the configured tests execute successfully.

If the test stage passes, the pipeline continues.

If an error occurs, Jenkins marks the pipeline as failed.

---

# 8. Jenkins Pipeline Stages

The Jenkins dashboard displays the pipeline stages.

The successful pipeline shows the stages completed successfully.

```text
┌──────────┐
│ Checkout │
└────┬─────┘
     ↓
┌────────────────────┐
│ Install Dependencies│
└────────┬───────────┘
         ↓
┌──────────┐
│  Build   │
└────┬─────┘
     ↓
┌──────────┐
│   Test   │
└────┬─────┘
     ↓
┌──────────┐
│ SUCCESS  │
└──────────┘
```

All pipeline stages were executed successfully.

---

# 9. Jenkins Console Output

The Jenkins **Console Output** was used to verify the execution of each pipeline stage.

The console output displays:

* Git repository checkout
* Dependency installation
* Build execution
* Test execution
* Pipeline stage execution
* Final build status

At the end of the execution, Jenkins displayed:

**Finished: SUCCESS**

This confirms that the complete pipeline executed successfully.

---

# 10. Successful Build

After all stages were completed successfully, Jenkins generated a successful build.

The Jenkins job showed the build number and successful execution status.

The successful build confirms that:

* Source code was successfully retrieved.
* Dependencies were installed.
* Build process completed successfully.
* Tests completed successfully.
* Jenkins pipeline completed without errors.

---

# 11. CI/CD Workflow

The complete CI/CD workflow implemented in this project is:

```text
Developer
    ↓
Write / Update Code
    ↓
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
Verify Result
    ↓
Successful Build
```

This automation reduces manual effort and provides a consistent software delivery process.

---

# 12. Screenshots

The following screenshots demonstrate the successful completion of the project:

### Screenshot 1 – GitHub Repository

Shows the project repository containing the application files and Jenkinsfile.

```text
[Add GitHub Repository Screenshot Here]
```

### Screenshot 2 – Jenkins Job / Build

Shows the Jenkins job and the executed build.

```text
[Add Jenkins Build Screenshot Here]
```

### Screenshot 3 – Jenkins Console Output

Shows the Jenkins console output with the pipeline execution details and successful result.

```text
[Add Jenkins Console Output Screenshot Here]
```

### Screenshot 4 – Jenkins Pipeline Stages

Shows all Jenkins pipeline stages completed successfully.

```text
[Add Jenkins Pipeline Stages Screenshot Here]
```

### Screenshot 5 – Successful Pipeline Execution

Shows the final successful Jenkins pipeline/build status.

```text
[Add Final Success Screenshot Here]
```

---

# 13. Result

The Jenkins CI/CD pipeline was successfully implemented and executed.

The pipeline successfully connected the GitHub repository with Jenkins and automated the application workflow from source-code checkout to build and testing.

The Jenkins console output and pipeline stages confirmed that the execution was successful.

**Final Status: SUCCESS ✅**

---

# 14. Conclusion

This project provided practical experience in implementing a CI/CD pipeline using Jenkins and GitHub.

By automating the build and testing process, Jenkins helps reduce manual work, detect errors earlier, and maintain a consistent software delivery workflow.

The successful execution of all Jenkins stages demonstrates that the CI/CD pipeline was configured and implemented correctly.
