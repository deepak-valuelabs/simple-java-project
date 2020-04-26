pipeline {
    agent {
        docker { image: 'maven:3-alpine' }
    }
    stages {
        stage('My-app-compile') {
            steps {
                checkout scm
                 sh 'mvn compile'
           }
        }  
        stage('My-app-test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('My-app-package') {
            steps {
                sh 'mvn package'
            }
        }
    }
} 
