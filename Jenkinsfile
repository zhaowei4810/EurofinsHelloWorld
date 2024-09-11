pipeline {
    agent any

    environment {
        PATH = "/usr/local/share/dotnet:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/zhaowei4810/EurofinsHelloWorld.git'
            }
        }

        stage('Build') {
            steps {
                sh 'dotnet restore'
                sh 'dotnet build'
            }
        }

        stage('Test') {
            steps {
                sh 'dotnet test'
            }
        }
    }
}
