pipeline {
    agent any
 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git url: 'http://nimbusserver.aos.com:8091/git/node-junit.git'
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