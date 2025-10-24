pipeline {
  agent any
  stages {
    stage('Echo version') {
      steps {
        sh 'echo Print maven version'
        sh 'mvn -version'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package -DskipTests=true'
      }
    }

    stage('Unit test') {
      steps {
        sh 'mvn test'
      }
    }

  }
  tools {
    maven 'M398'
  }
}