pipeline {
agent any
stages{
       
  stage('Build'){
    steps{
           mvnHome = tool 'M3'
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
