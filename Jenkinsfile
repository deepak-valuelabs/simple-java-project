pipeline{
    agent any 
    stages {
        stage ('git checkout') {
            steps {
                checkout scm
                sh 'mvn test'
            }
        }
        stage ('maven compile') {
            steps {
                sh 'mvn complie'
            }
        }
    }
}
                
