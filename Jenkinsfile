pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // This command checks out the source code from the configured SCM
                checkout scm
                  sh "pwd"
                    sh "hostname -i "
            }
        }

        stage('installing nginx') {
            steps { 
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh-21',keyFileVariable: 'ssh_key_file')]) {
                    sh '''
                       ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "hostname -i"
                         ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "sudo yum install nginx -y "
                         
                    '''
                }
               
            }
        }

        
    }
}
