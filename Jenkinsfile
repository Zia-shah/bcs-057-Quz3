
pipeline {
    agent any
    stages {
        stage('Build java') {
            steps {
                bat 'javac Hello.java'
                bat 'java Hello'
            }
        }
    }
}
