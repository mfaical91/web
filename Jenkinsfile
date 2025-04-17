pipeline {
    agent any
     tools {
        jdk 'jdk17'
        nodejs 'node16'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
