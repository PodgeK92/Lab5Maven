pipeline {
    agent any
    stages {
        stage ('GetProject') {
            steps {
                git 'https://github.com/PodgeK92/Lab5Maven.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn clean:clean'
                sh 'mvn dependency:copy-dependencies'
                sh 'mvn compiler:compile'
            }
        }
        stage ('Exec') {
            steps {
                sh 'mvn exec:java'
            }
        }
    }
}