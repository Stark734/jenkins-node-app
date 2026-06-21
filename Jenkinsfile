pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Stark734/jenkins-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Validate Code') {
            steps {
                sh 'node -c app.js'
            }
        }

    }

    post {
        success {
            echo 'CI Pipeline SUCCESS 🚀'
        }

        failure {
            echo 'CI Pipeline FAILED ❌'
        }
    }
}
