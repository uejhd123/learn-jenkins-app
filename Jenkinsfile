pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "w/o docker"'
                sh 'ls -la'
            }
        }
        stage('with docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh 'npm --version'
                sh 'ls -la'
            }
        }
    }
    
}
