pipeline {
    agent any
    stages {
      
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS695-1'
                    sh 'g++ -o file1 main/PES1UG22CS695.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './file1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying normally'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline has failed'
        }
    }
}
