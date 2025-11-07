pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('git clone') {
            steps {
                git url: 'https://github.com/spring-projects/spring-petclinic',branch: 'master'

            }
        }
        stage ('debug') {
            steps {
                sh 'pwd;ls -la'
            }
        }
        stage('build with maven') {
            steps {
                dir('app') {
                    sh 'pwd;ls -la'
                     sh 'mvn clean package'
                }
            }
        }
    }
}
