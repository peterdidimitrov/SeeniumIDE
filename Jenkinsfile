pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
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