### Getting started

Make sure that you have the Openshift Pipelines operator installed. The operator can be installed from the operator hub using the instructions [here](https://github.com/openshift/pipelines-tutorial/blob/master/install-operator.md). 

#### Create a new Namespace

`oc new-project tekton-task-run`

#### Install the Pipeline Resource

`oc create -f https://raw.githubusercontent.com/atef23/tkn-tsk-tst/master/simple-s2i-built-image.yaml`

#### Install the task

`oc create -f https://raw.githubusercontent.com/atef23/tkn-tsk-tst/master/workflows-s2i.yaml`


#### Run the task

`oc create -f https://raw.githubusercontent.com/atef23/tkn-tsk-tst/master/run.yaml`


This will start the task running. You can check the logs using `tkn pipeline logs -f` 
