pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o new.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG22CS695-1'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
