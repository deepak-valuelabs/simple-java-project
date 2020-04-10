pipeline {
    stages {
        stage('build') {
            agent { docker 'maven:3-alpine' }
            steps {
                checkout scm
                 sh 'mvn test'
           }
        }  
    }
}    
