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
                echo "Image tag is $IMAGE_TAG"
            }
        }
    }
}