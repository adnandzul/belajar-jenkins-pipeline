pipeline {
    agent none
    stages {
        stage('build') {
            agent {
                node {
                    label 'linux && java11'
                }
            }
            steps {
                echo 'start build!'
                sh './mvnw clean compile test-compile'
                echo 'end build!'
            }
        }

        stage('test') {
            agent {
                node {
                    label 'linux && java11'
                }
            }
            steps {
                script {
                    def data = [
                        'firstname': 'adnan',
                        'LastName': 'dzulfiqar'
                    ]
                    writeJSON(file: 'data.json', json: data)
                }
                echo 'hello test'
                sh './mvnw test'
                echo 'hello test'
            }
        }

        stage('Deploy') {
            agent {
                node {
                    label 'linux && java11'
                }
            }
            steps {
                echo 'hello Deploy'
                echo 'hello Deploy'
                echo 'hello Deploy'
            }
        }
    }

    post {
        always {
            echo 'always mw'
        }
        success {
            echo 'yay success'
        }
        failure {
            echo 'oh, shit'
        }
        cleanup {
            echo "Don't care success or error"
        }
    }
}
