pipeline {
    agent {
        label 'maven-slave'
    }
    environment {
        Applicant_Name = 'EUREKA'
    }
    stages {
        stage ('Build') {
          steps {
            echo "buliding the ${env.Application_Name} application"
            sh "mvn clean package -Dskiptests=true"
          }
        }
    }
}
