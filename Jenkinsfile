pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
            }
        }
    }

    stage('connecting web-server'){
        steps {
            withCredentials([sshUserPrivateKey(credentialsId: 'ssh-21', keyFileVariable: 'SSH_KEY')]) {
               sh 'ssh -i "${SSH_KEY}" -o StrictHostKeyChecking=no ec2-user@13.232.103.179 "hostname -i"'
            }
                                                        
        }
    }
}
