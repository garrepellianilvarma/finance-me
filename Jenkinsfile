pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source Code Checked Out'
            }
        }

        stage('Build') {
            steps {
                dir('finance-me') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                dir('finance-me') {
                    sh 'docker build -t finance-me:v1 .'
                }
            }
        }

    }
}
