
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building Java File'
                sh 'javac Hello.java'
            }
        }
        stage('Run') {
            steps {
                echo 'Running Java File'
                sh 'java Hello'
            }
        }
    }
}
