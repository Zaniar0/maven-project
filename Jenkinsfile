pipeline {
    agent any
    stages {
        stage('One') {
            steps{
                echo 'YOOO!!!! Bled'
                //bat 'mvn clean package'
            }
        }
        stage('Two') {
            steps{
                echo 'YOOO!!!! Zaniar'
                //bat 'mvn clean package'
            }
        }
    }
}
// Send Slack notification function
def sendSlackNotification()
    {
        // build status of null means successful
        buildStatus =  currentBuild.result

        // Default values
        def subject = "${buildStatus}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'"
        def summary = "${subject} (${env.BUILD_URL})"

        // Set notification color based on build status
        if (buildStatus == 'STARTED') {
            color = 'YELLOW'
            colorCode = '#FFFF00'

        } else if (buildStatus == 'SUCCESS') {
            color = 'GREEN'
            colorCode = '#00FF00'

        } else {
            color = 'RED'
            colorCode = '#FF0000'
        }

        // Set slack channel
        channel = "test-jenkins"

        // Send notifications
        slackSend (color: colorCode, message: summary, channel: "#${channel}" )
    }
