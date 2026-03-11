pipeline {
    agent any

    environment {
        APP_NAME = "DemoApp"
        BUILD_ENV = "Development"
    }

    options {
        timestamps()
    }

    stages {

        stage('Initialize') {
            steps {
                echo "Starting pipeline for ${APP_NAME}"
                echo "Environment: ${BUILD_ENV}"
            }
        }

        stage('Build') {
            steps {
                echo "Building application..."
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
                sh 'echo Creating application artifact'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh 'echo Deploying to staging server'
            }
        }

        stage('Monitor') {
            steps {
                echo "Monitoring deployment..."
                sh 'echo Checking application status'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully"
        }
        failure {
            echo "Pipeline execution failed"
        }
        always {
            echo "Pipeline finished"
        }
    }
}
