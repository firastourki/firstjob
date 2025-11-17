pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/firastourki/firstjob.git'
            }
        }

        stage('Build') {
            steps {
                dir('student-management') {
                    sh './mvnw clean install'
                }
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests"
            }
        }
    }
}

