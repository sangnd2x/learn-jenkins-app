pipeline {
    agent any
   
    stages {
        stage('Install Docker') {
            steps {
                script {
                    // Install Docker commands
                    sh '''
                        # Update the package manager
                        sudo apt-get update
                        
                        # Install Docker (example for Ubuntu)
                        sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common
                        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
                        sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
                        sudo apt-get update
                        sudo apt-get install -y docker-ce
                    '''
                }
            }
        }

        stage('Check Docker') {
            steps {
                sh '''
                    docker --version
                '''
            }
        }
    }
}
