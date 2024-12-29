pipeline {
    agent any

    environment {
        OCAML_VERSION = "4.14.0"
        OPAM_VERSION = "2.0.0"
    }

    stages {

        stage('Start') {
            steps {
                echo 'Starting pipeline...'
                echo "Build number is ${currentBuild.number}"
            }
        }

        stage('Build Project') {
            steps {
                dir('let') {
                    echo 'Building project...'
                    sh 'dune ut'
                }
            }
        }

        stage('Run Tests') {
            steps {
                dir('let') {
                    echo 'Running tests...'
                    sh 'dune runtest'
                }
            }

            post {
                success {
                    script {
                        currentBuild.result = 'SUCCESS'
                    }
                }
            }
        }

        stage('Clean Up') {
            steps {
                echo 'Cleaning up...'
                sh 'dune clean'
            }
        }
    }

    post {
        always {
            echo "Build result is ${currentBuild.currentResult}"
        }
        success {
            echo "Pipeline succeeded. Check the logs for details."
        }
        failure {
            echo "Pipeline failed. Check the logs for details."
        }
    }
}
