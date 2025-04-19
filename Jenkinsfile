pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo "Installing Node.js version 22..."
                sh '''
                    curl -fsSL https://rpm.nodesource.com/setup_22.x | sudo bash -
                    sudo dnf install -y nodejs
                    node -v
                '''
            }
        }
        stage('Build') {
            steps {
                echo "Simulating build process: displaying npm version..."
                sh 'npm --version'
            }
        }
        stage('Test') {
            steps {
                echo "Simulating test: printing JENKINS_URL environment variable..."
                sh 'echo "JENKINS_URL is $JENKINS_URL"'
            }
        }
    }
}
