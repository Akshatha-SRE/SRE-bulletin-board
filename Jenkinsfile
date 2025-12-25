pipeline {
    agent { label 'agent' }

    options {
        timestamps()
        disableConcurrentBuilds()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build started"
                sh 'date'
            }
        }

        stage('Validate') {
            steps {
                sh 'ls -la'
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS"
        }
        failure {
            echo "Pipeline FAILED"
        }
        always {
            echo "Pipeline FINISHED"
        }
    }
}

