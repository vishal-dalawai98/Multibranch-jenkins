pipeline {
    agent any

    stages {

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Build Success'
        }

        failure {
            echo 'Build Failed'
        }
    }
}
