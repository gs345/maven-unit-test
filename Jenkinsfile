pipeline {
    agent {
        label 'jenkins-jdk21'
    }
    stages {
        stage('Build') {
            steps {
                // Build the project, e.g., using Maven
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Run the tests
                sh 'mvn test'
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
