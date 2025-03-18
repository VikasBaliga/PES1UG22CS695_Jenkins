pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS695-1'
                sh 'g++ main/PES1UG22CS695.cpp -o main/PES1UG22CS695'
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
