pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the C++ file...'
                sh 'g++ -o PES1UG22CS377-1 newcppfile.cpp' 
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './PES1UG22CS377-1' 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
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
