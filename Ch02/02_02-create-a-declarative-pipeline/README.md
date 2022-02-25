# 02_02 Create a declarative pipeline

## Pipeline formats
Jenkins support two pipeline formats: Scripted and declarative.

For the rest of this course, we’ll be using the declarative format.

## Required sections in the pipeline configuration
A pipeline configuration has three required sections.

- `agent`
- `stages`
- at least one `stage` and at least one `step`

## A multi-stage pipeline
Create a pipeline job and paste in the following code to create a multi-stage pipeline:

```Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Requirements') {
            steps {
                echo 'Getting Requirements....'
            }
        }
        stage('Build') {
            steps {
                echo 'Building....'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..1'
                echo 'Testing..2'
                echo 'Testing..3'
            }
        }
        stage('Report') {
            steps {
                echo 'Reporting....'
            }
        }
    }
}
```
