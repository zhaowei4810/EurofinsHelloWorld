pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // 克隆代码
                git branch: 'master', url: 'https://github.com/zhaowei4810/EurofinsHelloWorld.git'
            }
        }

        stage('Build') {
            steps {
                // 使用 dotnet 执行构建
                sh 'dotnet restore'
                sh 'dotnet build'
            }
        }

        stage('Test') {
            steps {
                // 运行测试
                sh 'dotnet test'
            }
        }
    }
}
