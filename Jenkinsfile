pipeline {
    agent any 
    tools {
        maven: 'maven'
        jdk: 'JDK8'
    }
    stages {
        stage('build') {
            steps {
                echo 'bulding' 
                bat 'mvn clean'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy'
                bat 'nvm install'
            }
        }
    }
}
