pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://your-repo-url.git'
            }
        }

        stage('Build') {
            steps {
                // Compile the Java program
                sh 'javac Square.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                sh 'echo "5" | java Square'
            }
        }
    }

    post {
        always {
            // Clean up workspace after pipeline completion
            cleanWs()
        }
    }
}
