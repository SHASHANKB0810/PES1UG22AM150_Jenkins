pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o my_program my_program.cpp'
                    echo 'Build PES1UG22AM150 completed successfully'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './my_program'
                }
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
            echo 'Pipeline failed'
        }
    }
}
