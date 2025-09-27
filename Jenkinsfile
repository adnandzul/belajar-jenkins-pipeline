pipeline {
    agent none

    environtment {
        AUTHOR = 'adnan dzulfiqar'
        EMAIL = 'adnan@gnail.com'
        WEB = 'https://adnan.com'
    }
    stages {
        stage('prepare') {
            agent {
                node {
                    label 'linux && java11'
                }
            }
            steps {
                echo("author ${AUTHOR}")
                echo("email ${EMAIL}")
                echo("web ${EMAIL}")
                echo("Start Job : ${env.JOB_NAME}")
                echo("Start Build : ${env.BUILD_NUMBER}")
                echo("Branch name : ${env.BRANCH_NAME}")
            }
        }
        stage('build') {
            agent {
                node {
                    label 'linux && java11'
                }
            }
            steps {
                echo("Start Job : ${env.JOB_NAME}")
                echo("Start Job : ${env.JOB_NAME}")
                echo("Start Job : ${env.JOB_NAME}")
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
