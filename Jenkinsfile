pipeline {
    agent any

    stages {
        stage('Build') {
            agent{
                docker{}
                    imagine 'node:18-alpine'
                    resuseNod true
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
