pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("hello yuhu"){
            steps{
                echo("yuhuu this is step brow")
            }
        }
    }
    post {
        always {
            echo "awlyas mw"
        }
        success {
            echo" yay success"
        }
        failure {
            echo "oh, shit"
        }
        cleanup {
            echo " Don't care succes or error"
        }
    }
}