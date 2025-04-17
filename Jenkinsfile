
pipeline {
    agent any
    tools {
        jdk 'jdk17'
        nodejs 'node16'
    }
      stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
          stage("Sonarqube Analysis") {
            steps {
               echo "Sonarqube Analysis"
            }
        }
        stage('Install Dependencies') {
            steps {
                sh "npm install"
            }
        }
    }
}
