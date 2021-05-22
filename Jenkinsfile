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
            steps {
                script {
                    if (test==="TRUE") {
                        sh "mvn test"
                    }
                    else {
                        echo "disable"
                    }
                }
            }
        }
        stage("package my code") {
            steps {
                sh "mvn package"
            }
        }
    }
}
           
  
