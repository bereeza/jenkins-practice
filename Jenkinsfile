pipeline {
    agent any
    environment {
        NODE_VERSION = '22.0.0'
        NVM_DIR = "$HOME/.nvm"
    }
    stages {
        stage('Prepare') {
            steps {
                script {
                    sh '''
                    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
                    export NVM_DIR="$HOME/.nvm"
                    [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
                    
                    nvm install $NODE_VERSION
                    nvm use $NODE_VERSION
                    
                    which npm
                    npm -v
                    '''
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh '''
                    export NVM_DIR="$HOME/.nvm"
                    [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
                    nvm use $NODE_VERSION
                    npm -v
                    '''
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
