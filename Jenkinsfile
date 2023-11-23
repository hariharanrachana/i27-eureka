pipeline {
    agent {
        label 'maven-slave'
    }
    tools {
        
        jdk 'JDK-17'
      
    }
    environment {
        APPLICATION_NAME = "eureka"
    }
    stages {
        stage ('build') {
            steps {
            echo "Building the ${env.APPLICATION_NAME} application"
                // maven build should happpen here 
                sh "mvn clean package -DskipTests=true"
                
            }
        }
        stage ('Unit Tests'){
            steps {
                echo "Performing Unit Tests for ${env.APPLICATION_NAME} application"
                sh "mvn test"
            }
        }
    }
}
