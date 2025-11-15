pipeline {
    agent {
        docker {
            image 'mon-tp-python'
            args '-u root:root'
        }
    }
    stages {
        stage('Test Docker') {
            steps {
                sh 'python --version'
                sh 'echo "Salut Gianna ! Docker fonctionne !"'
            }
        }
        stage('Run Python Script') {
            steps {
                echo 'Lancement de Flask en arrière-plan...'
                sh 'python app.py & sleep 5'
                echo 'Flask a démarré temporairement pour le test.'
            }
        }
    }
    post {
        always {
            echo 'Pipeline terminé !'
        }
    }
}
