pipeline {
    agent {
        label 'jenkins-jdk21'
    }
    stages {
        stage('Build') {
            steps {
                // Build the project, e.g., using Maven
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Run the tests
                bat 'mvn test'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
