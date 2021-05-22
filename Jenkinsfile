pipeline {
    agent any
    stages {
        stage("checkout code") {
            steps {
                checkout scm
            }
        }
        stage("$action") {
            steps {
                sh "mvn $action"
            }
        }
    }
}
