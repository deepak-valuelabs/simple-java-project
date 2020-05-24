pipeline {
    agent any
    stages {
        stage ('test my code') {
               steps {
                   checkout scm 
                   sh 'mvn test'
               }
        }
        stage ('compile my code') {
            steps {
                sh 'mvn compile'
            }
        }
        stage ('approval') {
            steps {
                input ('Do you want to proceed')
            }
        }
        stage ('package my code') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
               
