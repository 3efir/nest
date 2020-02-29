pipeline {
    agent { label 'development' }

    stages {
        stage('Install project') {
            steps {
                sh 'cd nest'
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
