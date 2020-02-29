pipeline {
    agent { label 'development' }

    stages {
        stage('Checkout project') {
            steps { 
                git branch: '6.3.0', url: 'https://github.com/3efir/nest.git'
            }
        }
        stage('Install project') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'npm ci'
            }
        }
        stage('Build project') {
            steps {
                sh 'nmp run build'
            }
        }
        stage('Test project') {
            steps {
                sh 'npm run test'
            }
        }
    }
}
