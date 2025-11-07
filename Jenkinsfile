pipeline {
    agent any
    tools {
        jdk 'JDK17'
        maven 'Maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                // write your logic here
            git url: 'https://github.com/ponkarthika-ramesh/java-batch-job-example.git', branch:'main'
             }
        }
        stage('Build') {
            // write your logic here
            steps {
                 bat 'mvn clean install'
        }
        stage('Run Application') {
            // write your logic here
            steps {
                 bat 'start /B java -jar target\\java-batch-job-example.jar'
        }
        stage('Test') {
            // write your logic here
            steps {
                  'mvn test'
            }
        }
        stage('Post Build Notification') {
            // write your logic here
            steps {
                echo 'Build and Test completed successfully'
    }
    }
}
