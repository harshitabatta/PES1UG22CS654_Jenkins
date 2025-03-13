pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES1UG22CS654.cpp -o PES1UG22CS654-1'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS654-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
