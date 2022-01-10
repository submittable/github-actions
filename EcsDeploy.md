![image](https://www.libarts.colostate.edu/english/wp-content/uploads/sites/56/2019/10/Logo-Trans-Square-dc1c4a5d0772746ba773fd50374b673f.png)
# Submittable ECS Image Deploy Workflow

### 💻Runtime Environment: ### 
```Self hosted with Kubernetes Runners (Ubuntu 20.4) running internally in EKS```
### 💻K8 runner version: ### 
```2.286.0```
### ⚙️GitHub Actions: ###
```
+++++++++++++++Configure AWS Credentials
+++++++++++++++Checkout
+++++++++++++++Amazon ECS Render Task Definition
+++++++++++++++Amazon ECS Deploy Task Definition
+++++++++++++++Action Slack Notify
```
### 👷Pipeline workflow: ###
```
+++++++++++++++Choose available runner (self-hosted)
++++++++++++++++Checkout repo
+++++++++++++++++Augment Provided Task Def JSON with new Requested Image
+++++++++++++++++Deploy Task Defintion Update and wait for success
+++++++++++++++++Slack Notification - On Success
+++++++++++++++++Slack Notification - On Failure
```

## 💾How to Install in project

1. Create folder ```.github/workflows``` in the root directory of your repo

2. Create file ```ecs-deploy.yml``` and copy code from ```caller-examples/ecs-cd-caller.yml``` and save.

3. Edit file ```ecs-deploy.yml``` and update input values as identified in comments

4. Save and Create PR

5. Click ```Actions``` tab within repository and create new workflow

6. Manually execute the pipeline against a development environment

7. Feedback is sent to Slack ```builds``` channel once build is completed. Notification occurs on PR to ```main``` branch
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-23+at+6.21.39+PM.png)
