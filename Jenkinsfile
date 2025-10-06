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

      //  stage('installing nginx') {
        //    steps { 
          //      withCredentials([sshUserPrivateKey(credentialsId: 'slave-21',keyFileVariable: 'AppVM')]) {
            //        sh '''
              //          ssh -i '{$AppVM}' -o StrictHostKeyChecking=no ec2-user@13.201.28.185 "sudo yum install -y nginx"
                //    '''
               // }
               
           // }
       // }
    }
}
