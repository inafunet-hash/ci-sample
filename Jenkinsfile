pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'ls -la .'
                sh 'chmod +x test.sh'
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

