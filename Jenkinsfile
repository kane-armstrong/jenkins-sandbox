def majorVersion = '1'
def minorVersion = '0'

def imageTag = 'sandbox/jenkins-sandbox:${majorVersion}.${minorVersion}.{env.BUILD_NUMBER}'

pipeline {
    agent any
    environment {
        REGISTRY = 'registry.kanearmstrong.com'
        MAJOR_VERSION  = '0'
        MINOR_VERSION = '0'
    }
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build . -t ${imageTag}'
            }
        }
        stage('Publish Docker Image') {
            steps {
                sh 'docker push ${imageTag}'
            }
        }
    }
}