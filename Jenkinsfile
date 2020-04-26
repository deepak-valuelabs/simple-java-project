pipeline {
    agent any
    stages {
        stage('My-app-compile') {
            agent {
                docker { image 'maven:3-alpine' }
            }
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
