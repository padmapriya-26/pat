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
        stage('build with maven') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
