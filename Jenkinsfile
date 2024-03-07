pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                // Intentional error: Execute a non-existent script
                sh './non_existent_script.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            script {
                error 'Pipeline failed'
            }
        }
    }
}
