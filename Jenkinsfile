pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Set up Python') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install --upgrade pip'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '. venv/bin/activate && pip install unittest'
            }
        }

        stage('Run Tests') {
            steps {
                sh '. venv/bin/activate && python -m unittest test_main.py'
            }
        }

        stage('Run Program') {
            steps {
                sh '. venv/bin/activate && python main.py'
            }
        }
    }
}
