pipeline {
    agent any

    stages {
        stage('Credentials Test') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'sonal_Tester',
                        usernameVariable: 'sonal',
                        passwordVariable: 'sonal@2005'
                    )
                ]) {
                    echo "Username is: ${sonal}"
                    echo "Password is stored securely"
                }
            }
        }
    }
}