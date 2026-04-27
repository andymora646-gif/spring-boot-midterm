pipeline {
    agent any
    tools {
        maven 'Maven 3.x' // Make sure this matches your Jenkins tool config later
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Fat Jar') {
            steps {
                // This command creates the fat jar in the /target folder
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}
