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

        stage('build') {
            steps {
                echo 'Deploying....'
                bat 'mvn install'

            }
        }

        stage('deploy'){
            steps {
                echo 'deploy'
                deploy adapters: [tomcat9(credentialsId: 'deed08da-e729-499b-8112-10eec4e638a4', path: '', url: 'http://localhost:8080/')], contextPath: 'whatisthedate', war: 'target/*.war'
            }
        }
    }
}