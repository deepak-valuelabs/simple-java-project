pipeline{
    agent any 
    stages {
        stage ('git checkout') {
            steps {
                checkout scm
            }
        }
        stage ('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage ('maven test') {
            steps {
                sh 'mvn test'
            }
        }
        stage ('maven package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
                
