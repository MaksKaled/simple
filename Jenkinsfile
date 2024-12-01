pipeline {
    agent {
        docker {
            image 'node:16' // Используем Node.js 16
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/MaksKaled/simple.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }
}
