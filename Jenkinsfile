pipeline {
    agent any
    
    environment {
        OCAML_VERSION = "4.14.0"
        OPAM_VERSION = "2.0.0"
    }

    stages {
        stage('Build') {
            steps {
                dir('simple_interpreter/let') {
                    sh 'ls -la'
                }
            }
        }
    }
}
