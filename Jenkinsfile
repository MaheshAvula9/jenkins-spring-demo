pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t maheshavula83/jenkins-demo-app:latest .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker push maheshavula83/jenkins-demo-app:latest'
            }
        }
    }
}
