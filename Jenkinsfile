pipeline {
    agent any

    tools {
        maven 'Maven 3.9.9' 
        jdk 'JDK 21'
    }

    stages {
        stage('Build and Test') {
            steps {
                bat 'mvn clean test'
            }
        }
    }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
