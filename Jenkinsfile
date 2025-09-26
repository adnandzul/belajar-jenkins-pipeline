pipeline {
    agent { label "linux && java11" }

    stages {
        stage("build") {
            steps {
                script {
                    def data = [
                        "firstname": "adnan",
                        "LastName": "dzulfiqar"
                    ]
                    writeJSON(file: "data.json", json: data)
                }

                echo "start build!"
                sh "./mvnw clean compile test-compile"
                echo "end build!"
            }
        }

        stage("test") {
            steps {
                echo "hello test"
                sh "./mvnw test"
                echo "hello test"
            }
        }

        stage("Deploy") {
            steps {
                echo "hello Deploy"
                echo "hello test"
                echo "hello test"
            }
        }
    }

    post {
        always {
            echo "always mw"
        }
        success {
            echo "yay success"
        }
        failure {
            echo "oh, shit"
        }
        cleanup {
            echo "Don't care success or error"
        }
    }
}
