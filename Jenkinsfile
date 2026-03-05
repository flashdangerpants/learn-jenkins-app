pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "Hello DOCKERLESS World"'
            }
        }


        stage('with docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'echo "Hello DOCKER"'
                sh 'npm --version'
                
            }
        }
    }
}
