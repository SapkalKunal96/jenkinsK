pipeline {
    agent {
        label 'ubuntu-virtualbox'
    }
    environment {
        build_id = "${env.BUILD_ID}"
        git_owner = "${env.GIT_AUTHOR_NAME}"
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
        stage('Print hello world on label') {
            steps {
                echo "Hello World on label: ${env.NODE_LABELS}"
            }
        }
        stage('Print build id') {
            steps {
                sh "echo Build id is $build_id"
            }
        }
        stage('Print git owner') {
            steps {
                sh "echo Git owner is $git_owner"
            }
        }
    }
}
