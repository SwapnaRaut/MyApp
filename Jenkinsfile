pipeline{
 
		agent{
			
			label{

				label 'Slave-1'
			     
                              }	
	          	}

		stages{
			
			stage('install httpd'){

				steps{

					echo "installing httpd"
					sh "sudo yum install httpd -y"
				}
			}

	                stage('Start httpd'){

                                steps{

                                        echo "Start httpd"
                                        sh "sudo service httpd start"
					sh "sudo chkconfig httpd on"
                                }
                        }
			
			 stage('deploy index.html on httpd'){

                                steps{

                                        echo "Deploy index.html on httpd Server"
                                        sh "sudo cp -r /home/ec2-user/22Q1/index.html /var/www/html/"
					sh "sudo chmod -R 777 /var/www/html/"
                                    }
                        }
	
				
		}
}
				

		
