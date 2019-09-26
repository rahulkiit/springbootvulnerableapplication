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
              }
           } 
      }
        
 }
