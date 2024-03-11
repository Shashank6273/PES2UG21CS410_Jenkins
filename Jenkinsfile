pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o output PES2UG21CS410.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Execute the compiled output file
                    sh './output'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here
                echo 'Deployment completed'
            }
        }
    }
    
    post {
        always {
            // Display 'pipeline failed' in case of any errors within the pipeline
            echo 'Pipeline finished'
        }
    }
}
