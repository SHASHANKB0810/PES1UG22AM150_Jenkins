pipeline {
    agent any
    
    stages {
        stage('Test') {
    steps {
        script {
            sh './non_existent_program'  // Intentional error
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
