pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
            }
        }

         stage('connecting web-server'){
        steps {
            withCredentials([sshUserPrivateKey(credentialsId: 'ssh-05', keyFileVariable: 'SSH_FILE_KEY')]) {
               sh 'ssh -i "${SSH_FILE_KEY}" -o StrictHostKeyChecking=no ec2-user@65.2.190.207 "ls -lrt"'
                sh 'ssh -i "${SSH_FILE_KEY}" -o StrictHostKeyChecking=no ec2-user@65.2.190.207 "sudo yum install nginx -y"'
                sh 'ssh -i "${SSH_FILE_KEY}" -o index.html root@65.2.190.207:/usr/share/nginx/html/index.html' 
            }
                                                        
        }
    }
    }
}
