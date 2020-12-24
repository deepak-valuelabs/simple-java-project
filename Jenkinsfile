pipeline {
    agent any
    stages{
        stage('Application Build'){
            steps {
                checkout scm 
                sh "mvn compile"
            }
        }
        stage('test my code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package my Application'){
            when {
                expression {
                    env.deployment == 'TRUE'
                }
            }
            steps{
                sh 'mvn package'
                sh 'pwd'
                sh 'mkdir ${path}'
                sh 'cp -r /var/lib/jenkins/workspace/pipe-2323/* ${path}'
            }
        }
    }
}
