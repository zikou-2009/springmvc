pipeline {
agent any
stages{
       mvnHome = tool 'M3'
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
