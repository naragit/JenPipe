pipeline {
    agent any
    environment {
        IMAGE = "IMG_NAME"
        VERSION = "1.00"
    }
    stages {
        stage('build') {
            steps {
                bat 'npm --version'
            }
        }
        stage('test') {
            steps {
                bat 'java -version'
                echo " IMG:   ${IMAGE} "
                echo " VER:   ${VERSION} "
            }
        }
    }
post {
        failure {    // notify users when the Pipeline fails
           echo "Job Failed "
        }
           always {
            echo 'One way or another, I have finished'
        }
        success {
            echo " Post Completion "
        }
    }
}
