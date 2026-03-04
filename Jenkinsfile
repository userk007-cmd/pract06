pipeline {
    agent { label 'agent1' }

    stages {
        stage('Checkout') {
            steps {
                // Checkout from GitHub repo
                git branch: 'main', url: 'https://github.com/userk007-cmd/pract06.git'
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
    }
}
