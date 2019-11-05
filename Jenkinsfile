pipeline {
agent any
 environment {
   mvnHome = tool 'M3'
    }
stages{
   
  stage('Build'){
    steps{
      withEnv(["MVN_HOME=$mvnHome"]) {
      sh '"$MVN_HOME/bin/mvn" clean install'
      }
    }
  }
  }
}
