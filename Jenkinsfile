pipeline {
    agent any
    
    environment {
        OCAML_VERSION = "4.14.0"
        OPAM_VERSION = "2.0.0"
    }

    stages {
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
        }
    }

    post {
        always {
            echo "Pipeline finished"
        }
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline failed. Check the logs for details."
        }
    }
}
