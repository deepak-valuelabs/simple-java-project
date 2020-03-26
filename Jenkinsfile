pipeline {
    agent {
        docker {
            image '${myimage}'
        }
    }
    stages {
        stage('build') {
            steps {
                checkout scm 
                sh 'mvn test'
            }
        }
        
    }
}
