pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("build"){
            steps{
                echo("hello build!")
            }
        } 
        stage("test"){
            steps {
                echo("hello test")
            }
        }
        stage("Deploy"){
            steps {
                echo("hello Deploy")
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