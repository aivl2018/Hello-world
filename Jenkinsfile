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
            sh 'ssh -o StrictHostKeyChecking=no 72.31.45.184 -l ubuntu ; bash /home/ubuntu/bac.sh'
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
