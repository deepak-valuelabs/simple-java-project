pipeline {
    agent {
        docker { image 'maven:3-alpine' }
    }
    stages {
        stage('Build') { 
            steps {
                checkout scm
                sh 'mvn test'
            }
        }
        stage('Test') { 
            steps {
                checkout scm
                sh 'mvn compile'
            }
        }
        stage('Deploy') { 
            steps {
                checkout scm
                sh 'mvn package'
            }
        }
    }
}
