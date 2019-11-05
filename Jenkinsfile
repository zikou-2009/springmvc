pipeline {
agent any
stages{
  stage('Build'){
          mvnHome = tool 'M3'
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
