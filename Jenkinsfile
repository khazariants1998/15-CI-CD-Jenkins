pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo "Installing Node.js version 22..."
                // Для Ubuntu ключовим є встановлення через Debian пакети NodeSource:
                sh '''
                    curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
                    sudo apt-get install -y nodejs
                    node -v
                '''
            }
        }
        stage('Build') {
            steps {
                echo "Displaying npm version..."
                sh 'npm --version'
            }
        }
        stage('Test') {
            steps {
                echo "Displaying JENKINS_URL environment variable..."
                sh 'echo "JENKINS_URL is $JENKINS_URL"'
            }
        }
    }
}
