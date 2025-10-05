pipeline {
    agent { label 'slave-21'}

    stages {
          stage('Installing python') {
            steps {
                // This command checks out the source code from the configured SCM
                   sh "sudo yum install python3 python3-pip"
                    sh "pwd"
                   
            }
        }

            stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
                  sh "pwd"
            }
        }

    
    }
}
