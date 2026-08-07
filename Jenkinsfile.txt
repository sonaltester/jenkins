pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello Sonal'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Application'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Successful'
        }

        failure {
            echo 'Pipeline Failed'
        }

        always {
            echo 'Pipeline Finished'
        }
    }
}