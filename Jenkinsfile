pipeline {
    agent {
        docker {
            image 'node:16' 
            args '-u root'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install --save' 
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
