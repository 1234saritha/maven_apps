node {
   
   stage('Code Checkout') { 
     git credentialsId: 'githubID', url: 'https://github.com/itrainbatman/maven_apps.git' 
    }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn test'
      } 
    }
   stage('Sonar CodeAnalysis') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
        sh 'mvn sonar:sonar Dsonar.projectKey=com.sonar.practice -Dsonar.organization=collect -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=c57d9c7587386932f78c5a05405661d64e10ac09'
      }  
    }
   stage('Package to Jfrog') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
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
