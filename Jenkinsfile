pipeline {
    agent any
    environment {
        NODE_VERSION = '22.0.0'
    }
    stages {
        stage('Prepare') {
            steps {
                script {
                    sh '''
                    # Install NVM
                    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
                    export NVM_DIR="$HOME/.nvm"
                    [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"   
                    
                    # Install Node.js using NVM
                    nvm install $NODE_VERSION
                    nvm use $NODE_VERSION
                    '''
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
                    sh 'echo $JENKINS_URL'  
                }
            }
        }
    }
}
