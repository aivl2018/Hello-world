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
          sh('hostname -i')    
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
