pipeline {
  agent any
  tools{
      maven 'M2_home'
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
     echo "deploy step"
    sleep 10
    }
  } 
    stage ('docker') {
    steps {
     echo " image step"
    sleep 10
    }
  } 
 }
}





