pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url:'https://github.com/ancylazar/jenkins-parameter-pipeline.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat '"C:\\Users\\ANCY LAZAR\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}