pipeline {
    agent {
        label 'static-agent'
    }
    tools {
        nodejs 'nodejs-setup'
        maven 'maven-setup'
    }

    stages {
        stage('Build') {
            steps {
                echo 'build in progress...'
                sh 'node -v'

            }
        }

        stage('Test') {
            steps {
                echo 'test in progress...'
                sh 'mvn -v'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy in progress.00..'
            }
        }
    }
}