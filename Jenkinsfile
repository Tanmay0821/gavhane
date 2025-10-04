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

        stage('installing nginx') {
            steps { 
                withCredentials([sshUserPrivateKey(credentialsId: 'slave-21',
                                                  keyFileVariable: 'AppVM')]) {
                    sh '''
                        ssh -i "$AppVM" -o StrictHostKeyChecking=no ec2-user@65.1.131.143 \
                        "sudo yum install -y nginx"
                    '''
                }
               
            }
        }


           

    }
}
