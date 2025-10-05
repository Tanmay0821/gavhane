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
                echo "this is rahul"
                sh "ls -lrt" 
            }
        }

          stage('coping code') {
            steps {
               // sh "sudo mkdir /opt/python-08"
                sh "sudo cp /home/ec2-user/jenkins2/workspace/Test/first-jen-job/sample.py /opt/python-08/sample.py"
                sh "sudo cp /home/ec2-user/jenkins2/workspace/Test/first-jen-job/requirements.txt /opt/python-08/requirements.txt"
                sh " cd /opt/python" 
                sh "nohup python3 sample.py > abc 2>&1 &"
                
            }
        }

    
    }
}
