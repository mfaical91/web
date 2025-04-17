pipeline {
    agent any
    tools {
        jdk 'jdk17'
        nodejs 'node16'
    }
    stages {
        stage('Setup') {
            steps {
                git url: 'https://github.com/votre-repo.git'
                sh 'java -version'  // Vérifie JDK
                sh 'node -v'        // Vérifie Node.js
            }
        }
        stage('Build Frontend') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Build Backend') {
            steps {
                sh 'javac -d ./target ./src/*.java'  // Exemple pour Java
            }
        }
    }
}
