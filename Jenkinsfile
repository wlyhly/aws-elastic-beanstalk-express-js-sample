pipeline {
    agent {
        docker {
            image 'node:16'  // Use Node 16 Docker image as the build agent
            args '-u root'   // Run as root user for permissions in Docker
        }
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install --save'  // Run npm install command
            }
        }
    }
    
    post {
        success {
            echo 'Build successful!'
        }
        
        failure {
            echo 'Build failed!'
        }
    }
}
