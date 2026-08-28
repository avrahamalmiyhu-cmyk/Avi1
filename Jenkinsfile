pipeline {
    agent {
        // מריץ את הפייפליין על ה-Worker לפי התגית שהגדרת לו
        node {
            label 'Linux-docker'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
                checkout scm
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // כאן ירוצו בדיקות יחידה או בדיקות סקריפט
                sh 'echo "Testing code syntax..."'
            }
        }

        stage('Build') {
            steps {
                echo 'Building artifact or Docker image...'
                sh 'echo "Build finished successfully"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished!'
        }
        success {
            echo 'Everything passed!'
        }
        failure {
            echo 'Something failed!'
        }
    }
}
