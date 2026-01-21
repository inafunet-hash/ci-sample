pipeline {
    agent any

    stages {
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

