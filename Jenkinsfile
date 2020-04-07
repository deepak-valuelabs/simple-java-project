pipeline{
    agent any 
    stages {
        stage ('git checkout') {
            steps {
                checkout scm
                sh 'mvn test'
            }
        }
    }
}
                
