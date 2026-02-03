pipeline {
    agent {
        label 'static-agent'
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
                sh 'npm -v'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy in progress.00..'
            }
        }
    }
}