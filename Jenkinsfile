pipeline {
  options {
    buildDiscarder(logRotator(numToKeepStr: '5')) 
  }
  
  agent none
  
  stages {
    stage('Build') {
      agent {
        docker {
          image "localhost:31095/gradle:3.5-jdk8-alpine"
        }
      }
      steps {
        sh 'gradle build'
      }
    }
  }
}