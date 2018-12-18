#!groovy
pipeline {
  agent { label 'master' }
  environment {
    DOCKER_HOST = "tcp://docker-builder.hi.inet:4243"
    DOCKER_API_VERSION = "1.21"
   
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '20'))
  }
  stages {
    stage('build and push') {
      when {
        expression { env.BRANCH_NAME == 'develop' }
      }
      steps {
        sh "echo Empezando"
        
      }
      post {
        always {
          sh "echo adios"
        }
      }
    }
    stage('build and push release') {
      when {
        expression { true != false }
      }
      steps {
        sh "echo Build and release"
        
      }
      post {
        always {
          sh "echo adios"
        }
      }
    }
  }
}
