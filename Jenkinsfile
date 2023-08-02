pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Checkout your code from version control (e.g., Git)
                // Run npm install and other build tasks here
                docker build -t nodejs .
            }
        }

    }
}
