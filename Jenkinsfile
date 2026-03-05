pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo "Cloning repository"
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }

        stage('Build') {
            steps {
                echo "Build completed"
            }
        }

    }

    post {
        success {
            echo "Pipeline completed successfully"
        }

        failure {
            echo "Pipeline failed"
        }
    }
}
