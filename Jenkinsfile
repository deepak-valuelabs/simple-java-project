pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                sh 'echo hello'
            }
        }
        stage('test1') {
            steps {
                sh 'echo $TEST'
            }
        }
        stage('test3') {
            steps {
                script {
                    if (env.TEST == 'TRUE') {
                        echo 'I only execute on the master branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
