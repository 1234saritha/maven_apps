node {
   
   stage('Code Checkout') { 
     git credentialsId: 'githubID', url: 'https://github.com/1234saritha/maven_apps.git' 
    }
   stage('Build') {
    withMaven(jdk: 'jdk-1.8', maven: 'maven') {
     sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'jdk-1.8', maven: 'maven') {
     sh 'mvn test'
      } 
    }
   
   
   stage('Deploy to Dev') {
     
    }
   stage('Automation Testing') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Smoke Testing') {
     
    }
   stage('Deploy to Prod') {
     
    }
   stage('Acceptance Testing') {
     
    }
}
