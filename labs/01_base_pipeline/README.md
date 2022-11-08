# Create a base pipeline

This folder holds the files for the lab _Create a Base Pipeline_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

```
$ kubectl apply -f task.yaml
$ kubectl apply -f pipeline.yaml
$ tkn pipeline start --showlog hello-pipeline
$ tkn pipeline start cd-pipeline \
>     --showlog \
>     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
>     -p branch="main"
PipelineRun started: cd-pipeline-run-ml6s4
Waiting for logs to be available...
[clone : checkout] Cloning into 'wtecc-CICD_PracticeCode'...

[lint : echo-message] Calling Lint

[tests : echo-message] Testing code from main

[build : echo-message] Building image for https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git
[deploy : echo-message] Deploying code from main
    
```
