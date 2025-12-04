pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Fetching source code..."
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo "Installing Node dependencies..."
                bat "npm install"   
              
            }
        }

 
        stage('Run Tests') {
            steps {
                echo "Running tests..."
                bat "npm test"   
               
            }
        }

        stage('Docker Build') {
            steps {
                echo "Building Docker image..."
                bat "docker build -t todo-app ."   
                
            }
        }
    }
}
