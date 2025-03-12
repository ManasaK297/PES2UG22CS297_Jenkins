pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output main/hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
