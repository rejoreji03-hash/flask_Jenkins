pipeline {
    agent any

    stages {

        stage('Check Environment') {
            steps {
                sh 'python3 --version'
                sh 'python3 -m pip --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }

        stage('Build') {
            steps {
                sh 'mkdir -p build'
                sh 'cp app.py build/'
                sh 'cp requirements.txt build/'
            }
        }
    }
}