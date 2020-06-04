# Jenkins Hands-on CRV

This is a project created for a short hands-on session with Jenkins for CRV.

### Step 1: Clone the repository

clone the repo using ssh:
`git clone git@github.com:willlie1/crv_jenkins_handson.git`

or Https:
`git clone https://github.com/willlie1/crv_jenkins_handson.git`

### Step 2: create your own branch

create a branch like: 
`feature/{your_name}`

Use any tool or execute the following from the commandline:
`git checkout -b feature/{your_name}`

Push your branch!
`git push`

Now check http://jenkins-handson-crv.eastus.cloudapp.azure.com/job/jenkins-handson-crv/. As you can see, your branch is not building yet. We'll fix that in the next step!


### Step 3: create a jenkinsfile

By creating a Jenkinsfile, we "tell" jenkins to do something with this branch.
In the root dir of your project, create a file named `Jenkinsfile`, so this would become `{path_to_your_project}/crv_jenkins_handson/Jenkinsfile`

Now commit this Jenkinsfile and push your branch:

`git commit Jenkinsfile -m "Adding initial Jenkinsfile" && git push`

Now check again: http://jenkins-handson-crv.eastus.cloudapp.azure.com/job/jenkins-handson-crv/. As you can see, your branch is being build! However, since our Jenkinsfile is empty, it does not do anything yet.

### Step 4: Creating your own pipeline

A pipeline consists of different stages as you may have seen in all jenkins jobs of CRV. So we are building our own here!

For any information about Jenkinsfiles please go to: https://www.jenkins.io/doc/book/pipeline/jenkinsfile/

While developing your pipeline, keep in mind the best-practices: https://www.jenkins.io/doc/book/pipeline/pipeline-best-practices/

What I want you to try: 

1. create a declarative pipeline which contains the following stages: `clean`, `test`, `build`, `deploy`
2. create a scripted pipeline which contains the following stages: `clean`, `test`, `build`, `deploy`
3. create a scripted pipeline using groovy which contains the following stages: `clean`, `test`, `build`, `deploy`

EXTRA:
- Try to add some validation i.e. correct version. Make sure it fails when it should!

**Note**: The `deploy` step cannot be executed during this demo, instead we will just Log the following string: "Yay, we've deployed our application using a jenkins pipeline"

To help you a little, we've created some branches with examples for each step.

PS: Make sure to push after you've made changes, Jenkins will only see what you've pushed!

