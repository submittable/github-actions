# Submittable GitHub Action Reusable Workflow 2.0

This repository contains github reusable workflows for Nodejs and Python projects. It runs tests and Sonar scan on the project.

## How to Install on project

1. Create a ```.github/workflows``` folder within the root directory

2. Create file ```workflow.yml``` and copy code from ```reusable-workflow-caller/reusable-workflow.yml```

3. Change the ```repo_name``` in line 19 of ```workflow.yml``` file to the project name. This will consumed by Sonar scanner

4. Save and Create PR

5. Check Actions tab within repository and confirm that workflow is running 
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+10.48.28+AM.png)


## Manual Run
1. Go to your Actions tab and click on the workflow eg: ```Resuable Workflow 2.0```
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+10.48.28+AM.png)

2. Click on ```Run workflow``` drop down menu and choose which branch you want to run manually
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+11.27.49+AM.png)