pipeline {
    agent any
    triggers {
        pollSCM('* * * * *') // Poll every minute
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/peterdidimitrov/SeeniumIDE'
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