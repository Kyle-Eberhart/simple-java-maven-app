pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'M3'
    }

    stages {
        stage('Long Running Step') {
  steps {
    sh 'echo "Starting long step..."'
    sh 'sleep 1000'
    sh 'echo "Finished long step."'
  }
}
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
