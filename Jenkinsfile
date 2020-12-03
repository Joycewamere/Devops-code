pipeline {
  agent any
  tools{
      maven 'M2_home'
  }
  environment {
     registry= "wamere/devops-pipeline"
     registry credential= "Docker2.0ID"
  }
  stages {
   stage ('Build') {
    steps {
      sh 'mvn clean'
      sh 'mvn install'
      sh 'mvn package'
    } 
   } 
    stage ('test') {
    steps {
      sh 'mvn test'
    }
  } 
    stage ('deploy') {
    steps {
     script
      docker.build registry + ":$BUILD_NUMBER"
    sleep 10
    }
  }
 }
}





