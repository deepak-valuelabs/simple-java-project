pipeline {
    agent any
    stages {
        stage ('compile job for my code') {
               steps {
                   checkout scm 
                   sh 'mvn compile'
               }
        }
        stage ('test case run') {
            steps {
                sh 'mvn test'
            }
        }
        stage ('package my code') {
            steps {
                sh 'mvn package'
                
            }
        }
    }
}
               
