pipeline {
    agent any
    tools {
        go '1.19'
    }

    environment {
        GO111MODULE='on'
        CGO_ENABLED='0'
    }

    stages{
        stage('Build'){
            steps{
               git 'https://github.com/AdminTurnedDevOps/go-webapp-sample.git'
               sh 'go build .'
            }
        }

        stage('Run'){
            steps {
                sh 'cd /var/lib/jenkins/workspace/go-full-pipeline && go-webapp-sample &'
            }

        }
    }
}
