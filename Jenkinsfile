pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run --rm my-app test-command'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker push my-app'
            }
        }
    }
}
