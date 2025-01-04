pipeline {
    agent {
        docker {
            image 'node:16.0.0-alpine'
        }
    }
    stages {
        stage('test version') {
            steps {
                sh 'node --version'
            }
        }
    }
}
