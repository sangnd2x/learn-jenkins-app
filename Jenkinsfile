pipeline {
    agent {
        docker {
            image 'docker:latest' // Use the Docker-in-Docker image
            args '-v /var/run/docker.sock:/var/run/docker.sock' // Share the Docker socket
        }
    }

    stages {
        stage('Check Docker Version') {
            steps {
                script {
                    // Check Docker version
                    sh 'docker --version'
                }
            }
        }
    }
}
