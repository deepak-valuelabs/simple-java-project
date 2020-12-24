pipeline {
    agent any
    stages{
        stage('Application Build'){
            steps {
                checkout scm 
                sh "mvn build"
            }
        }
        stage('test my code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package my Application'){
            steps{
                sh 'mvn package'
                sh 'pwd'
                sh 'mkdir /root/dpk'
                sh 'cp -r * /root/dpk/'
            }
        }
    }
}
