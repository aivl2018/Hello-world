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
           sh "ssh ubuntu@172.31.45.184 ' bash /home/ubuntu/bac.sh '"
          }
        }
        stage('Deploy') {
            steps {
                sh 'pwd'
            }
        }
    }
}
