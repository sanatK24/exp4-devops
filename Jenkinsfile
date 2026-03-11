pipeline {
    agent any

    environment {
        APP_NAME = "DemoApp"
    }

    options {
        timestamps()
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${APP_NAME}..."
                sh 'echo Compiling source code'
                sh 'java -version'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo Executing unit tests'
            }
        }

        stage('Package') {
            steps {
                echo "Packaging application..."
                sh 'echo Creating build artifact'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME}..."
                sh 'echo Deployment to test environment'
            }
        }

        stage('Monitor') {
            steps {
                echo "Monitoring application..."
                sh 'echo Checking application health'
            }
        }

    }

    post {
        success {
            echo "Pipeline executed successfully"
        }
        failure {
            echo "Pipeline failed"
        }
        always {
            echo "Pipeline execution finished"
        }
    }
}
