pipeline {
    agent any

    tools {
        jdk 'JDK23'    // Remplacer par votre version de JDK configurée
        maven 'apache-maven-3.9.9' // Remplacer par votre version de Maven configurée
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Run') {
            steps {
                sh 'mvn exec:java'
            }
        }
    }

    post {
        success {
            echo 'Pipeline exécuté avec succès!'
        }
        failure {
            echo 'Pipeline échoué!'
        }
    }
}