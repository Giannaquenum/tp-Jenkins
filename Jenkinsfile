pipeline {
    agent any

    stages {

        stage('Test Docker') {
            steps {
                sh 'which docker'
                sh 'docker --version'
                sh 'echo "Salut Gianna ! Docker fonctionne !"'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mon-tp-python .'
            }
        }

        stage('Run Python Script') {
            steps {
                sh """
                    docker run --rm \
                        -p 5000:5000 \
                        -v "$WORKSPACE":/app \
                        -w /app mon-tp-python \
                        python app.py
                """
            }
        }
    }
}

