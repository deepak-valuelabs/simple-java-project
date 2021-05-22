pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                checkout scm
                sh 'mvn compile'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('test3') {
            steps {
                script {
                    if (env.TEST == 'TRUE') {
                        sh 'mvn test'
                    } else if (env.TEST == 'FALSE') {
                        echo ' set to FALSE'
                    }
                    else (env.TEST == 'DISABLE') {
                        echo "set to disable'
                    }
                }
            }
        }
    }
}
