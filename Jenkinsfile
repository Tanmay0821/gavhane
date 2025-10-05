pipeline {
    agent { label 'slave-21'}

    stages {
        stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
                  sh "pwd"
                    sh "hostname -i "
            }
        }

    
    }
}
