pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Sai-Ashish24/Online_Bookstore.git'
            }
        }
        stage('HTML Lint') {
            steps {
                // Install tidy (HTML checker) - works if Jenkins agent has access
                sh 'sudo apt-get install -y tidy' // Only if you use Linux agent
                // Run HTML check on your Book.html
                sh 'tidy -errors Book.html || true'
            }
        }
    }
}
