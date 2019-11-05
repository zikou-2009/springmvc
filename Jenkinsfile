pipeline {
agent any
stages{
       def mvnHome
   stage('preparation') { // for display purposes
       steps{
      git 'https://github.com/zikou-2009/springmvc.git'
     mvnHome = tool 'M3'
              }
   }
  stage('Build'){
    steps{
      withEnv(["MVN_HOME=$mvnHome"]) {
      sh '"$MVN_HOME/bin/mvn" clean install'
      }
    }
  }
  stage('Test'){
    steps{
        withEnv(["MVN_HOME=$mvnHome"]) {
      sh '"$MVN_HOME/bin/mvn" test'
      }
    }
  }
}
}
