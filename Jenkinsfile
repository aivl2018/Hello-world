pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                sh 'pwd'
            }
        }
        stage('Test'){
        def a = 'echo bhushan > bhushan'
        sshagent(['dev_server']) {
            sh 'ssh -o StrickHostKeyChecking=no ubuntu@172.31.45.184 ${a}'
        }

        }
        stage('Deploy') {
            steps {
                sh 'pwd'
            }
        }
    }
}
