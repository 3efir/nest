pipeline {
    agent { label 'development' }

    stages {
        stage('Check npm version') {
            steps {
                sh 'npm --version'
            }
        }
    }
}