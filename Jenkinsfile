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
            if (test=="TRUE") {
                sh "mvn test"
            }
            else (test=="FALSE") {
                echo "Test case not preferred"
            }
//            else (test=="DISABLE") {
//                echo "Test is disabled"
//            }
            }
        }
        stage("package my code") {
            steps {
                sh "mvn package"
            }
        }
    }
}
           
  
