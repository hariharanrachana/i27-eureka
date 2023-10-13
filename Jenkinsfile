pipeline {
    agent {
        label 'maven-slave'
    }
    environment {
        Applicant_Name = 'EUREKA'
    }
    tools {
        maven 'maven-3.8.8'
        jdk 'jdk-17'
    }
    stages {
        stage ('Build') {
          steps {
            echo "buliding the ${env.Application_Name} application"
            sh "mvn clean package -Dskiptests=true"
            archiveArtifacts artifacts: 'target/*jar', followSymlinks: false
          }
        }
        stage ('unit test'){
            steps {
                echo "Performing unit tests for ${env.Application_Name} application"
                sh "mvn test"
            }
        }
    }
}
