pipeline {
    agent any
    tools{
        maven 'maven'
        jdk 'JDK8'}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'mvn clean'

            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                bat 'mvn install'

            }
        }
    }
}