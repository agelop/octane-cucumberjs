pipeline {
    agent any
 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git url: 'https://github.com/agelop/octane-cucumberjs.git'
                sh 'npm --version'
                sh 'npm install --save-dev'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            junit '*.xml'
        }
    }
}