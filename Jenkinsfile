pipeline {
    agent any
    stages {
        stage('Clonage du dépôt GitHub') {
            steps {
                git 'https://github.com/DavidBohorquez/OSDetector.git'
            }
        }

        stage('Installation de Pip et de Python') {
            steps {
                sh 'apt-get update'
                sh 'apt-get install -y python3 python3-pip'
                sh 'python3 -m pip install --upgrade pip'
            }
        }

        stage('Run Script') {
            steps {
                // Exécuter le script Python
                sh 'python3 OSDetector.py'
            }
        }
    }
}