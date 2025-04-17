
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
        stage("quality gate") {
            steps {
                script {
                    waitForQualityGate abortPipeline: false, credentialsId: 'Sonar-token'
                }
            }
        }
        stage('Install Dependencies') {
            steps {
                sh "npm install"
            }
        }
    }
}
