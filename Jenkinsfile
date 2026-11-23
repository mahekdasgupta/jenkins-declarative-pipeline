pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'Maven3'
    }

    stages {
        stage('Build') {
            steps {
                dir('app') {
                    git url: 'https://github.com/jenkins-docs/simple-java-maven-app',
                        branch: 'master'
                    bat 'mvn -B clean compile'
                }
            }
        }

        stage('Test') {
            steps {
                dir('app') {
                    bat 'mvn -B test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment simulation completed successfully.'
            }
        }
    }
}
