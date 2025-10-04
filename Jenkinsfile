pipeline {
    agent { label 'slave-21'}

    stages {
        stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
            }
        }

           stage('Checkout Code') {
            steps {
                     sh "pwd"
                    sh "hostname -i "
            }
        }

    }
}
