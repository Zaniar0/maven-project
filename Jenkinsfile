pipeline {
    agent any
    stages {
        stage('build') {
            steps{
                sh ' echo $pwd'
                sh 'mvn clean package'
            }
        }
    }
}
