pipeline {
    agent any

    tools {
        nodejs 'NodeJS-18'
    }

    stages {
        stage('1. Checkout Code') {
            steps {
                echo 'Fetching code from GitHub...'
                checkout scm
            }
        }

        stage('2. Install Dependencies') {
            steps {
                echo 'Installing npm packages...'
                bat 'npm install'
            }
        }

        stage('3. Run Tests') {
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('4. Build Success') {
            steps {
                echo 'Node.js application pipeline completed successfully!'
            }
        }
    }
}