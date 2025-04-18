pipeline {
    agent any

    tools {
        gradle 'gradle-8'  // Name from the Gradle installation in Jenkins
    }

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/KisanthS/jenkins-java-test.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Test Report') {
            steps {
                junit '**/build/test-results/test/*.xml'  // Path to test results
            }
        }
    }
}
