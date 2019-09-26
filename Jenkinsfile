pipeline {
    agent any
  
    stages {
          stage('Preparation') { 
              steps {
              sh 'apk add maven'
              sh 'apk add --no-cache openjdk8'
              }
           } 
         stage('Security Checks') {
                parallel {
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
        stage('Build and Release') { 
              steps {
              echo "Push build artifact in repository"
              }
           }
      }
        
 }
