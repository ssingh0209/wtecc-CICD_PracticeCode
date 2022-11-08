# Adding GitHub Triggers

This folder holds the files for the lab: _Adding GitHub Triggers_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

```
$ kubectl apply -f tasks.yaml
$ kubectl apply -f pipeline.yaml

$ tkn task ls
NAME       DESCRIPTION   AGE
checkout                 2 minute ago
echo                     2 minute ago

$ tkn pipeline ls
NAME          AGE             LAST RUN   STARTED   DURATION   STATUS
cd-pipeline   2 minutes ago   ---        ---       ---        ---

$ kubectl apply -f eventlistener.yaml

$ tkn eventlistener ls
NAME          AGE             URL                                                    AVAILABLE
cd-listener   9 seconds ago   http://el-cd-listener.default.svc.cluster.local:8080   True

$ kubectl apply -f triggerbinding.yaml
$ kubectl apply -f triggertemplate.yaml

$ kubectl port-forward service/el-cd-listener  8090:8080
Forwarding from 127.0.0.1:8090 -> 8080
Forwarding from [::1]:8090 -> 8080

$ curl -X POST http://localhost:8090 \
  -H 'Content-Type: application/json' \
  -d '{"ref":"main","repository":{"url":"https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode"}}'
  
$ tkn pipelinerun ls
NAME                    STARTED          DURATION   STATUS
cd-pipeline-run-hhkpm   10 seconds ago   ---        Running

$ tkn pipelinerun logs --last
[clone : checkout] Cloning into 'wtecc-CICD_PracticeCode'...

[lint : echo-message] Calling Flake8 linter...

[tests : echo-message] Running unit tests with PyUnit...

[build : echo-message] Building image for https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode ...

[deploy : echo-message] Deploying master branch of https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode ...
```
