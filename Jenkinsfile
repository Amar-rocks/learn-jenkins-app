pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:alpine:3.18.9'
                    reuseNode true
                }
            }
            steps {
                sh '''
                   ls -la
                   node --version
                   npm --version
                   npm ci
                   npm run build
                '''
            }
        }
    }
}