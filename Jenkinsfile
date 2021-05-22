pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                checkout scm
                sh 'mvn compile'
            }
        }
        stage('test on condition') {
            steps {
                script {
                    if (env.TEST == 'TRUE') {
                        sh 'mvn test'
                    } else if (env.TEST == 'FALSE') {
                        echo 'set to FALSE'
                    }
                    else (env.TEST == 'DISABLE') {
                        echo 'set to disable'
                    }
                }
            }
        }        
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
