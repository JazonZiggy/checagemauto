pipeline {
    agent {
        docker {
            
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    }
        environment { 
                HTTP_PROXY = 'http://proxy:3128'
                HTTPS_PROXY = 'http://proxy:3128'
                http_proxy = 'http://proxy:3128'
                https_proxy = 'http://proxy:3128'
                NO_PROXY = 'docker'
                no_proxy = 'docker'
            }

    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
