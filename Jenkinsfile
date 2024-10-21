pipeline {
    agent any
    triggers {
        pollSCM('H/1 * * * *') // Poll every minute
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo-url.git'
            }
        }
        stage('Build project') {
            steps {
                bat 'dotnet build'
            }
        }
        stage('Execute Tests') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}