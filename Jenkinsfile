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
                         ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "pwd"
                       ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "hostname -i"
                     ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "sudo yum install nginx -y"
                    ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "sudo systemctl enable nginx" 
                    ssh -i "${ssh_key_file}" -o StrictHostKeyChecking=no ec2-user@13.127.252.144 "sudo rm -rf /usr/share/nginx/html/*"
                    scp -o StrictHostKeyChecking=no -r Jenkinsfile README.md a.txt tanmay.html ec2-user@13.127.252.144:/usr/share/nginx/html/ 
                    '''
                }
               
            }
        }

        
    }
}
