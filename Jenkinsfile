def majorVersion = '1'
def minorVersion = '0'

def imageTag = 'sandbox/jenkins-sandbox:${majorVersion}.${minorVersion}.{env.BUILD_NUMBER}'

pipeline {
    agent any
    stages {
        stage('Test') {
            echo 'Image tag is ${imageTag}'
        }
    }
}