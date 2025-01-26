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
                    ls -la
                    mode --version
                    npm --version
                    npm ci
                    npm run build  
                '''    
            }
        }
    }
}
