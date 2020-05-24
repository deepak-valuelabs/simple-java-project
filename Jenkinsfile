pipeline {
    agent any
    stages {
        stage ('test my code') {
               steps {
                   checkout scm 
                   sh "${command}"
               }
        }
    }
}
               
