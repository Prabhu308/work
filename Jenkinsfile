pipeline {
    agent any

    environment {
        NODE_HOME = tool name: 'nodejs', type: 'NodeJSInstallation'
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Clone') {
            steps {
                // Clone the repository from GitHub
                git 'https://github.com/Prabhu308/work.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Install Node.js dependencies
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                // Run tests (if you have any)
                // You can replace this with your test command
                echo 'No tests to run'
                // Uncomment the line below if you have tests
                // sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the application
                echo 'Deploying the application...'
                // Add your deployment commands here
                // For example, you can use scp to copy files to a server
                // sh 'scp -r * user@yourserver:/path/to/your/web/root'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}