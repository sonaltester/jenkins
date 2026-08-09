pipeline {
    agent any

    stages {
        stage('Credentials Test') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'sonal-demo-creds',
                        usernameVariable: 'MY_USER',
                        passwordVariable: 'MY_PASS'
                    )
                ]) {
                    echo "Username is: ${MY_USER}"
                    echo "Password is stored securely"
                }
            }
        }
    }
}