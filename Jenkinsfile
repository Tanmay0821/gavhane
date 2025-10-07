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
            }
        }

          stage('coping code') {
            steps {
                sh "sudo mkdir /opt/python"
                sh "sudo cp /home/ec2-user/jenkins2/workspace/Tanmay/tanmay-slave/sample.py /opt/python/sample.py"
                sh "sudo cp /home/ec2-user/jenkins2/workspace/Tanmay/tanmay-slave/requirements.txt /opt/python/requirements.txt"
                sh " cd /opt/python" 
                sh "nohup python3 sample.py &"
                
            }
        }

    
    }
}

