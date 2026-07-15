pipeline {

    agent any

    tools {
        go 'gotest'
    }

    environment {
        GO111MODULE='on'
    }

    stages {

        stage('Test') {

            steps {

                git 'https://github.com/SkNazeef09/ci-cd-test-script.git'

                sh 'go test ./...'

            }

        }

        stage('Build') {

            steps {

                git 'https://github.com/SkNazeef09/ci-cd-test-script.git'

                sh 'go build .'

            }

        }

        stage('Run') {

            steps {

                sh 'cd /var/lib/jenkins/workspace/full-cicd-go && go-webapp-sample &'

            }

        }

    }

}
