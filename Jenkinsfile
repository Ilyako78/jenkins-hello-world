pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        
        stage('Echo version'){
            steps{
                sh 'echo Print maven version'
                sh 'mvn -version'
            }
        }
        stage('Build'){
            steps{
                //git 'http://139.84.159.194:5555/dasher-org/jenkins-hello-world.git'
                //git 'https://github.com/sidd-harth/jenkins-hello-world.git'
                //git branch: 'main', url: 'https://github.com/Ilyako78/jenkins-hello-world'
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage('Unit test'){
            steps{
                sh "mvn test"
            }
        }
        
 
    }
}
