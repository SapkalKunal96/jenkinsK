pipeline {
    agent {
        label 'ubuntu-virtualbox'
    }
    environment {
        build_id = "${BUILD_ID}"
        git_owner = "${GIT_AUTHOR_NAME}"
    }
    stages {
        stage('test version') {
            agent {
                docker {
                    image 'node:16.0.0-alpine'
                }
            }
            steps {
                sh 'node --version'
            }
        }
        stage('Print hello world on "${label}"') {
            steps {
                sh 'echo "Hello World"'
            }
        }
        stage('Print build id') {
            steps {
                sh 'echo "Build id is $build_id"'
            }
        }
        stage('Print git owner') {
            steps { 
                sh 'echo Git owner is "$git_owner"'
            }
        }

    }
}
