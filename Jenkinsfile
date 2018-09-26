pipeline {
    agent any
    stages {
        stage('build') {
            steps{
                echo 'YOOO!!!! Bled'
                echo 'look out for --> $MVNLOCATION <--'
                sh '${env.mvn}" clean package'
            }
        }
    }
}
