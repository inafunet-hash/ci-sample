pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/inafunet-hash/ci-sample.git'
            }
        }

        stage('Test') {
            steps {
                sh './test.sh'
            }
        }
    }

    post {
        success {
            echo 'CI succeeded'
        }
        failure {
            echo 'CI failed'
        }
    }
}

