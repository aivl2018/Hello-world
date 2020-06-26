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
            steps {
              sshagent(['172.31.45.184']) {
                sh 'pwd'
                sh 'hostname -i'
            }
            }
        }
        stage('Deploy') {
            steps {
                sh 'pwd'
            }
        }
    }
}
