pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                
                sh 'curl -fsSL https://deb.nodesource.com/setup_22.x | bash -'
                sh 'apt-get install -y nodejs'
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
