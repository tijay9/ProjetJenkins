pipeline {
    agent any

    tools {
        jdk 'JDK17'    // Remplacer par votre version de JDK configurée
        maven 'apache-maven-3.9.9' // Remplacer par votre version de Maven configurée
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Run') {
            steps {
                bat 'mvn exec:java'
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
