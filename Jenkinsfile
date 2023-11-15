pipeline {
    agent {
        label 'maven-slave'
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
    }
}
