pipeline {
    agent any
    stages {
        stage("checkout code") {
            steps {
                checkout scm
            }
        }
        stage("compile") {
            steps {
                sh "mvn compile"
            }
        }
        stage("test my code on condition") {
            when {
                expression {
                    env.test == 'TRUE'
                }
            }
            steps {
                sh "mvn test"
            }
        }
        stage("package my code") {
            steps {
                sh "mvn package"
            }
        }
    }
}
           
  
