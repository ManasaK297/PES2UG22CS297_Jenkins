pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                shhh 'g++ -o output main/hello.cpp'
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
