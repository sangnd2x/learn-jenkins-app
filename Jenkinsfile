pipeline {
   agent {
        docker {
            image 'docker:latest'
            args '--privileged' // Required for Docker-in-Docker
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
