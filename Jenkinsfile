pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output hello.cpp'  // Compile C++ file
            }
        }
        
        stage('Test') {
            steps {
                sh './output'  // Execute compiled file
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline Failed!'  // Post action for failures
        }
    }
}
