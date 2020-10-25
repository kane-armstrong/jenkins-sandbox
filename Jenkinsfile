pipeline {
    agent any
    stages {

        def majorVersion = '1'
        def minorVersion = '0'

        def imageTag = 'sandbox/jenkins-sandbox:${majorVersion}.${minorVersion}.{env.BUILD_NUMBER}'

        stage('Test') {
            echo 'Image tag is ${imageTag}'
        }
    }
}