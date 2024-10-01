pipeline {
    agent any

    stages {
        stage('Check Docker Version') {
            steps {
                script {
                    // Check Docker version
                    sh 'sudo systemctl status docker'
                }
            }
        }
    }
}
