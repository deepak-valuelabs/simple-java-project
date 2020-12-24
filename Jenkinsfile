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
            steps{
                sh 'mvn package'
                sh 'pwd'
                sh 'mkdir /var/lib/jenkins/dpk'
                sh 'cp -r /var/lib/jenkins/workspace/Anil_pipeline_2/* /var/lib/jenkins/dpk'
            }
        }
    }
}
