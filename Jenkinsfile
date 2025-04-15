pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venvbinactivate && pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh '. venvbinactivate && pytest tests'
            }
        }
    }
}
