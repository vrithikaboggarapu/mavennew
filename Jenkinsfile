pipeline {
    agent any

    tools {
        maven 'Maven-Homebrew'  // 👈 Must match the name you configured 
in Jenkins > Tools
    }

    stages {
        stage('Checkout') {
            steps {
                echo '📦 Checking out code...'
                checkout scm
            }
        }

        stage('Build with Maven') {
            steps {
                echo '⚙️ Running Maven build...'
                sh 'mvn -B clean install'
            }
        }
    }

    post {
        success {
            echo '✅ Build completed successfully!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}



