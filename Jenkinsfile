pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/home/tounga/maven3/bin/mvn clean install'
            }           
        }
        stage('Test') {
            steps {
                sh '/home/tounga/maven3/bin/mvn test'
            }           
        }
    }
}
