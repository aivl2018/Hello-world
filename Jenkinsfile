pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                git credentialsId: '721943eb-b319-4836-af39-0639ef6e2ee2', url: 'https://github.com/aivl2018/Hello-world.git'
            }
        }
        stage('Connect_with_dev'){
          steps {   
           sshagent(['new-dev']) {
                sh """
                ssh -o StrictHostKeyChecking=no -l ubuntu 172.31.45.184 uname -a
                ssh ubuntu@172.31.45.184 hostname
                """
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
