pipeline {
    agent any

    stages {
        stage('build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    la -la
                    mode --version
                    npm --version
                    npm run build
                    ls -la
                    npm ci
                '''    
            }
        }
    }
}
