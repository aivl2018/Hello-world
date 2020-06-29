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
        sshagent(['dev_server1']) {
            sh 'ssh -o StrictHostKeyChecking=no ubuntu@172.31.45.184'    
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
