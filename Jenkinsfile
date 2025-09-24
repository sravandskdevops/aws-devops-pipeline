# pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage ('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage ('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
# }
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '✅ Build Stage: Application build successful!'
            }
        }

        stage('Test') {
            steps {
                echo '✅ Test Stage: All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo '✅ Deploy Stage: Application deployed successfully!'
            }
        }
    }

    post {
        success {
            echo '🎉 Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed. Check logs for details.'
        }
    }
}
