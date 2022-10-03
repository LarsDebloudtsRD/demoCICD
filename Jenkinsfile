pipeline {
    agent any
    tools{
        maven 'maven'
        jdk 'JDK8'}

    stages {
        stage('Build') {
            steps {
                echo 'mvn clean ...'
                bat 'mvn clean'

            }
        }

        stage('build') {
            steps {
                echo 'mvn install ...'
                bat 'mvn install'

            }
        }

        stage('deploy'){
            steps {
                echo 'deploy'
                deploy adapters: [tomcat9(credentialsId: 'deed08da-e729-499b-8112-10eec4e638a4', path: '', url: 'http://localhost:1112/')], contextPath: 'whatisthedate', war: 'target/*.war'
            }
        }
    }
}