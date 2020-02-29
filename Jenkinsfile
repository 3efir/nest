pipeline {
    agent { label 'development' }

    stages {
        stage('Install project') {
            steps {
                sh 'npm ci'
            }
        }
        stage('Build project') {
            sh 'nmp run build'
        }
        stage('Test project') {
            sh 'npm run test'
        }
    }
}
