![image](https://www.libarts.colostate.edu/english/wp-content/uploads/sites/56/2019/10/Logo-Trans-Square-dc1c4a5d0772746ba773fd50374b673f.png)
# Submittable Universal Reusable Workflow 2.0

This repository contains github actions reusable workflows for CI/CD projects.

### 💻Runtime Environment: ### 
```Self hosted with Kubernetes Runners (Ubuntu 20.4) running internally in EKS```
### 💻K8 runner version: ### 
```2.286.0```
### 💻Python version: ###
```3.6```
### 💻NodeJS version: ###
```15.x```
### 💻.Net version: ###
```5.0.x```
### ⚙️GitHub Actions: ###
```
+++++++++++++++Docker
+++++++++++++++QEMU
+++++++++++++++Docker Buildx
+++++++++++++++GitHub Container Registry
+++++++++++++++File Checker
+++++++++++++++Nodejs
+++++++++++++++Python
+++++++++++++++.Net
+++++++++++++++SemVer
+++++++++++++++Bumb and Tag version
+++++++++++++++Docker Publish to GitHub Registry
+++++++++++++++Slack
```
### 👷Pipeline workflow: ###
```
+++++++++++++++Choose available runner (self-hosted)
++++++++++++++++Checkout repo
+++++++++++++++++Set up QEMU
+++++++++++++++++Set up Docker Buildx
++++++++++++++++Login to GitHub Container Registry
++++++++++++++++Set Build Type using file extensions (Nodejs, Python, .Net)
+++++++++++++++++Run Tests (if test files are present)
++++++++++++++++Sonar Scan for vulnerabilities (Output in Sonar UI). Slack alert coming soon...
+++++++++++++++++Bump version and push tag
+++++++++++++++++Extract source branch/pr name
+++++++++++++++++Extract metadata (tags, labels)
++++++++++++++++Build, Tag and Push Docker Image
+++++++++++++++++Slack Notification - On Success
+++++++++++++++++Slack Notification - Dockerfile not Present
+++++++++++++++++Slack Notification - On Failure
```

### ✏️Pipeline workflow Diagram ###
![image](https://joseph-project-files.s3.amazonaws.com/Universal+Workflow.png)

## 💾How to Install in project

1. Change ```master``` branch to ```main``` to allow for Semantinc Release

2. Create folder ```.github/workflows``` in the root directory of your repo

3. Create file ```ci.yml``` and copy code from ```reusable-workflow-caller/reusable-workflow.yml``` and save.

4. Edit file ```ci.yml``` and make changes where necessary where you see ```#CHANGE```

5. Save and Create PR

6. Click ```Actions``` tab within repository and confirm that workflow is running successfully
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+10.48.28+AM.png)
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-23+at+7.17.39+PM.png)

7. Sonarqube Scan
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-23+at+7.24.59+PM.png)

8. Feedback is sent to Slack ```builds``` channel once build is completed. Notification occurs on PR to ```main``` branch
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-23+at+6.21.39+PM.png)


## ⚙️Manual Run
1. Go to your Actions tab and click on the workflow eg: ```Resuable Workflow 2.0```
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+10.48.28+AM.png)

2. Click on ```Run workflow``` drop down menu and choose which branch you want to run manually
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+11.27.49+AM.png)