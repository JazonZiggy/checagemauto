pipeline {
    agent {
        docker {
            environment { 
                HTTP_PROXY = 'http://proxy:3128'
                HTTPS_PROXY = 'http://proxy:3128'
                http_proxy = 'http://proxy:3128'
                https_proxy = 'http://proxy:3128'
            }
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}