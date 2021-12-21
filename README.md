# Submittable GitHub Action Reusable Workflow 2.0

This repository contains github reusable workflows for Nodejs and Python projects. It runs tests and Sonar scan on the project.

## How to Use

1. Create a ```.github/workflows``` folder within the root directory

2. Create file ```workflow.yml``` and copy code from ```reusable-workflow-caller/reusable-workflow.yml```

3. Change the ```repo_name``` in line 19 of ```workflow.yml``` file to the project name. This will consumed by Sonar scanner

4. Save and Create PR

5. Check Actions tab within repository and confirm that workflow is running 
![image](https://joseph-project-files.s3.amazonaws.com/Screen+Shot+2021-12-21+at+10.48.28+AM.png)
