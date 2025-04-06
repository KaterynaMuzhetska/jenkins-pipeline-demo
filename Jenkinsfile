pipeline {
    agent any

    stages {
        stage('Prepare') {
            steps {
                echo 'Installing Node.js v22...'
                sh '''
                    curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
                    sudo apt-get install -y nodejs
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Checking npm version...'
                sh 'npm --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Displaying JENKINS_URL...'
                sh 'echo $JENKINS_URL'
            }
        }
    }
}
