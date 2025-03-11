pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o my_program my_program.cpp'
                    echo 'Build YOUR_SRN-1 completed successfully'
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
