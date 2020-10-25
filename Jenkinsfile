def majorVersion = '0'
def minorVersion = '0'

pipeline {
    agent any
    environment {
        MAJOR_VERSION = '0'
        MINOR_VERSION = '0'
        IMAGE_TAG = "sandbox/jenkins-sandbox:${env.MAJOR_VERSION}.${env.MINOR_VERSION}.${env.BUILD_NUMBER}"
    }
    stages {
        stage('Test') {
            steps {
                echo "Image tag is $IMAGE_TAG"
            }
        }
    }
}