def majorVersion = '1'
def minorVersion = '0'

def imageTag = 'sandbox/jenkins-sandbox:${majorVersion}.${minorVersion}.{env.BUILD_NUMBER}'

pipeline {
    agent any
    environment {
        MAJOR_VERSION = '0'
        MINOR_VERSION = '0'
        IMAGE_TAG = 'sandbox/jenkins-sandbox:${majorVersion}.${minorVersion}.{env.BUILD_NUMBER}'
    }
    stages {
        stage('Test') {
            steps {
                echo 'Image tag is ${imageTag}'
            }
        }
    }
}