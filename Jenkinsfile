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
                echo "Image tag is $env.REGISTRY/$IMAGE_TAG"
            }
        }
        stage('Build image') {
          steps{
            script {
              dockerImage = docker.build "$env.REGISTRY/$IMAGE_TAG"
            }
          }
        }
        stage('Push image') {
          steps{
            script {
              docker.withRegistry( '', $env.REGISTRY_CREDENTIAL ) {
                dockerImage.push()
              }
            }
          }
        }
        stage('Cleanup images') {
          steps{
            sh "docker rmi "$env.REGISTRY/$IMAGE_TAG"
          }
        }
    }
}