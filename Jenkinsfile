pipeline {
    agent {
        docker { image 'maven:3-alpine' }
    }
    stages {
        stage('complie') {
        steps {
            sh 'mvn compile'
           }
        }
    }
}
            


