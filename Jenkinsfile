pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'M3'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -v'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
