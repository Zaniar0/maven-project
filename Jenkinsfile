pipeline {
    agent any
    stages {
        stage('build') {
            steps{
                echo '$pwd'
                sh 'mvn clean package'
            }
        }
    }
}
