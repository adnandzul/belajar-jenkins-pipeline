pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("build"){
            steps{
                script {
                    for (int i =0; i < 10; i++) {
                        echo("script ${i}")
                    }
                }
                echo("start build!")
                sh("./mvnw clean compile test-compile")
                echo("end build!")
            }
        } 
        stage("test"){
            steps {
                echo("hello test")
                sh("./mvnw test")
                echo("hello test")
            }
        }
        stage("Deploy"){
            steps {
                echo("hello Deploy")
                echo("hello test")
                echo("hello test")
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