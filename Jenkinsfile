pipeline {
    agent { label 'agent1' }   // Use your agent node label

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/userk007-cmd/pract06.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'   // Use 'sh' if agent is Linux
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'           // Use 'sh' if agent is Linux
            }
        }
    }
}