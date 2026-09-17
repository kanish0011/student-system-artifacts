pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com<your-username>/student-system-artifacts.git'
            }
        }
        stage('Generate Report') {
            steps {
                bat 'python student_report.py'
            }
        }
        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'academic_report.txt', fingerprint: true
            }
        }
    }
}
