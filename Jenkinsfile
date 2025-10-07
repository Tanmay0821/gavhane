pipeline {
    agent { label 'slave-08'}

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
                echo "this is rahul"
                sh "ls -lrt" 
                sh "ps -ef "
            }
        }

        //  stage('coping code') {
         //   steps {
              //  sh "sudo mkdir /opt/python-1"
              //  sh "sudo cp /home/ec2-user/jenkins2/workspace/Tanmay/tanmay-slave/sample.py /opt/python-1/sample.py"
            //    sh "sudo cp /home/ec2-user/jenkins2/workspace/Tanmay/tanmay-slave/requirements.txt /opt/python-1/requirements.txt"
          //      sh " cd /opt/python-1" 
            //    sh "nohup python3 sample.py &"
        //    }
      //  }

       // stage('kill'){
         //   steps{
         //       sh "kill -9 "    
       //     }
     //   }

        
    }
}

