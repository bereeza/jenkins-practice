pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                script {
                    sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -'
                    sh 'sudo apt-get install -y nodejs'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'npm -v' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'echo "$JENKINS_URL"'  
                }
            }
        }
    }
}

