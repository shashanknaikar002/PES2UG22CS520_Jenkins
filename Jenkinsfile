pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ -o hello_exec hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './hello_exec'  // Executes the compiled C++ program
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Check the error logs.'
        }
    }
}
