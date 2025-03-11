pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building new.cpp...'
                sh 'g++ -o new_exec new.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running new_exec...'
                sh './new_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage (placeholder)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Check the logs.'
        }
    }
}
