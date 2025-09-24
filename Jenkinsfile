pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build the Java project with Maven, skipping tests
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                // Run the tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // For now just echo, or you can copy .jar/.war to a server
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo '🎉 Maven pipeline completed successfully!'
        }
        failure {
            echo '❌ Maven pipeline failed. Check logs for details.'
        }
    }
}
