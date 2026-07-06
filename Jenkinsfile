pipeline {
    agent {
        label 'linux-agent'
    }

    stages {

        stage('Stage 1 - Checkout') {
            steps {
                echo "Running on node: ${env.NODE_NAME}"
                echo "Checking out source code..."
            }
        }

        stage('Stage 2 - Build') {
            steps {
                sh '''
                    echo "Building the application..."
                    pwd
                    ls -l
                '''
            }
        }

        stage('Stage 3 - Test') {
            steps {
                sh '''
                    echo "Running tests..."
                    echo "All tests passed."
                '''
            }
        }
    }

    post {
        always {
            echo "Pipeline execution completed."
        }

        success {
            echo "Pipeline executed successfully."
        }

        failure {
            echo "Pipeline execution failed."
        }
    }
}
