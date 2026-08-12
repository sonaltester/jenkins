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

// ------------------------------------------enviroment varibale/Build parameter -------------------------
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
                echo "Selected Environment: ${params.ENVIRONMENT}" //ye add karke build parameter ka value show karenge
                echo "Build Number: ${BUILD_NUMBER}"
                echo "Job Name: ${JOB_NAME}"
                echo "Workspace: ${WORKSPACE}"
                echo "ngrok URl"
            }
        }
        stage('Show Application') {
            steps {
                echo "Application Name: ${params.APP_NAME}"
            }
        }
        stage('Test') {
            when {
                expression {
                    params.RUN_TESTS
                }
            }
            steps {
                echo 'Testing Application'
            }
        }

        stage('Test run ') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Build'){
            step{
                bat 'mvn  clean package'
            }
        }
        
        }
    
}