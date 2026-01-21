pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh 'sed -i "s/\\r$//" test.sh'
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

