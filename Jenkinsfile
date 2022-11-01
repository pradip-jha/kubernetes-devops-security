pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "apt-get update"
              sh "sudo apt install openjdk-11-jdk -y"
              sh "java -version"
              sh "sudo apt install -y maven"
              sh "mvn -v"
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar'             
            }
        }   
    }
}