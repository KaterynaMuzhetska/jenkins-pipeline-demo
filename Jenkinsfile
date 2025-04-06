pipeline {
    agent any  // This specifies that the pipeline can run on any available agent.

    environment {
        NODE_VERSION = '22'
    }

    stages {
        stage('Prepare') {
            steps {
                script {
                    echo "Installing Node.js version ${env.NODE_VERSION}"
                    sh "curl -sL https://deb.nodesource.com/setup_${env.NODE_VERSION}.x | sudo -E bash -"
                    sh "sudo apt-get install -y nodejs"
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    echo "Building with npm version"
                    sh "npm -v"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "Running tests and displaying JENKINS_URL"
                    echo "Jenkins URL: ${env.JENKINS_URL}"
                }
            }
        }
    }
}
