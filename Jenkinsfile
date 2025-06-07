pipeline {
    agent any

    tools {
        maven 'maven' // Ensure this matches the Maven name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Bhagyalakshmi-R2005/Hello23.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -jar target\\MavenToAzure-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
