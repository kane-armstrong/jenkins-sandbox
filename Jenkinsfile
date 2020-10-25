pipeline {
    agent any
    environment {
        MAJOR_VERSION = '0'
        MINOR_VERSION = '0'
        IMAGE_TAG = "sandbox/jenkins-sandbox:${env.MAJOR_VERSION}.${env.MINOR_VERSION}.${env.BUILD_NUMBER}"
    }
    stages {
        stage('Report version number') {
            steps {
                echo "Image tag is $IMAGE_TAG"
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build . -t $IMAGE_TAG'
            }
        }
        stage('Publish Docker Image') {
            steps {
                sh 'docker push $IMAGE_TAG'
            }
        }
    }
}