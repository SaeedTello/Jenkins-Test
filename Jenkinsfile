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
    post {
        success {
            slackSend channel: '#jenkins-channel', color: '#b40078', message: "Build Success - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)", teamDomain: 'jenkinsworksp-ieq7351', tokenCredentialId: 'slack-notifiy'
        }
        failure {
            slackSend channel: '#all-jenkins-workspace', color: '#b40078', message: "Build Failed - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)", teamDomain: 'jenkinsworksp-ieq7351', tokenCredentialId: 'slack-notifiy'
        }
    }
}
