pipeline {
    agent any
    stages {
        stage('build') {
            steps{
                Echo 'priting current working directory'
                echo $PWD
                sh 'mvn clean package'
            }
        }
    }
}
