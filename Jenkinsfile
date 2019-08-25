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
   stage('Sonar CodeAnalysis') {
     withMaven(jdk: 'jdk-1.8', maven: 'maven') {
        sh 'mvn sonar:sonar -Dsonar.projectKey=maven_apps -Dsonar.organization=itrainbatman -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=0767bb0a33926d7ea765c0ef95c6f8d67cdd5987'
      }  
    }
   stage('Package to Jfrog') {
    withMaven(jdk: 'jdk-1.8', maven: 'maven') {
     sh 'mvn package'
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
