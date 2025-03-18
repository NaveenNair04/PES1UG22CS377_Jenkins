pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean package'
                echo 'Build stage successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
                echo 'Test stage successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh './deploy.sh'
                echo 'Deploy stage completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline Failed'
        }
    }
}
