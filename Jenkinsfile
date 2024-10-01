pipeline {
    agent any

    stages {
        stage('Run in Docker') {
            steps {
                script {
                    docker.image('docker:19.03.12').inside('--privileged') {
                        sh 'docker --version'
                    }
                }
            }
        }
    }
}