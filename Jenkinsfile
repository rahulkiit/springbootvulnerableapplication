pipeline {
    agent any
  
    stages {
          stage('Preparation') { 
              steps {
              sh 'apk add maven'
              sh 'apk add --no-cache openjdk8'
              }
           } 
        
             stage('Dependency Check') { 
              steps {
              sh 'mvn dependency-check:check'
              }
           } 
        
            stage('Static Code Analysis') { 
              steps {
              sh 'mvn spotbugs:check'
              }
           } 
      }
        
 }
