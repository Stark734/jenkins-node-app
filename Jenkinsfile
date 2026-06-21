pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Stark734/jenkins-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test / Validate') {
            steps {
                sh 'node -c app.js'
            }
        }

    }
}
