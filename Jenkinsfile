pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh 'sh test.sh'
            }
        }

        stage('Build') {
            steps {
                sh 'zip -r dist.zip dist'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'dist.zip', fingerprint: true
            echo 'CD artifact archived'
        }
        failure {
            echo 'CI/CD failed'
        }
    }
}
