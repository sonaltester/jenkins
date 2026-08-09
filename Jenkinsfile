// credentials practical
// pipeline {
//     agent any

//     stages {
//         stage('Credentials Test') {
//             steps {
//                 withCredentials([
//                     usernamePassword(
//                         credentialsId: 'sonal_Tester',
//                         usernameVariable: 'sonal',
//                         passwordVariable: 'sonal@2005'
//                     )
//                 ]) {
//                     echo "Username is: ${sonal}"
//                     echo "Password is stored securely"
//                 }
//             }
//         }
//     }
// }

// ------------------------------------------enviroment varibale -------------------------
pipeline {
    agent any

    environment {
        APP_NAME = 'SonalApp'
        ENVIRONMENT = 'TEST'
    }

    stages {
        stage('Show Environment') {
            steps {
                echo "Application: ${APP_NAME}"
                echo "Environment: ${ENVIRONMENT}"
                echo "Build Number: ${BUILD_NUMBER}"
                echo "Job Name: ${JOB_NAME}"
                echo "Workspace: ${WORKSPACE}"
            }
        }
    }
}