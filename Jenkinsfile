pipeline {
    agent { label 'development' }

    stages {
        stage('Checkout project') {
            checkout([$class: 'GitSCM', branches: [[name: '*/6.3.0']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/3efir/nest.git']]])
        }
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
