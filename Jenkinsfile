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
        stage('Test'){
          steps {   
           sh 'echo bhusuhan'
          }
        }
        stage('Deploy') {
            steps {
                sh 'pwd'
            }
        }
    }
}
