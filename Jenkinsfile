pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo "Pulling latest HTML code from GitHub..."
                checkout scm
            }
        }

        stage('Deploy Website') {
            steps {
                echo "Deploying HTML files..."
                sh '''
                    mkdir -p deploy
                    cp -r * deploy/
                '''
            }
        }
    }

    post {
        success {
            echo "HTML Website Deployed Successfully!"
        }
    }
}
