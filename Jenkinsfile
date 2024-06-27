pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: '79bf3068-f4e9-4249-ba4a-91dfc4002404', url: 'https://github.com/pranjal485/pranjal_01.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Building...'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                sh 'echo Testing...'
                // Add your test steps here
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying...'
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Cleanup steps
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
