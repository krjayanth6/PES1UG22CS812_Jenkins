pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                sh 'g++ -o output_binary YOUR_SRN-1.cpp'
            }
        }
        stage('Test') {
            steps {
                // Print the output of the compiled binary
                sh './output_binary'
            }
        }
        stage('Deploy') {
            // Define deployment steps if needed
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        always {
            // Display 'pipeline failed' in case of any errors within the pipeline
            echo 'Pipeline failed'
        }
    }
}
