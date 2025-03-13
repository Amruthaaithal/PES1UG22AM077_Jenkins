pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    echo 'Cloning repository...'
                    checkout scm
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o PES1UG22AM077-1 task5.cpp'  // Compile with SRN-based name
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh './PES1UG22AM077-1'  // Print output of compiled file
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                }
            }
        }
        
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
