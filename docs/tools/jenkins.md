# Jenkins Cheat Sheet

Jenkins is an open-source automation server for CI/CD.

## Installation (Docker)

The easiest way to run Jenkins is via Docker:

```bash
docker run -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```

Access it at `http://localhost:8080`.

## Jenkinsfile (Declarative Pipeline)

Create a `Jenkinsfile` in your repository:

```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'make build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh './deploy.sh'
            }
        }
    }
}
```