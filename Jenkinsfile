pipeline {
    agent any
    environment {
            registry = "rahulkiit/vulnerabledockerimage"
            registryCredential = 'dockerhub'
            dockerImage = ''
        }
    stages {
          stage('Preparation') { // for display purposes
              steps {
              sh 'apk add maven'
              sh 'apk add --no-cache openjdk8'
              }
           } 
        
             stage('Dependency Check') { // for display purposes
              steps {
              sh 'mvn dependency-check:check'
              }
           } 
        
            stage('Dependency Check') { // for display purposes
              steps {
              sh 'mvn spotbugs:check'
              }
           } 
      }
        
 }
