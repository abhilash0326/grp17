pipeline{
			agent {
					label{ 
						label 'built-in'
						customWorkspace '/data'
							}
			}
		stages{
	
				stage('Install apache'){
				
					steps{
							sh "yum install httpd -y"
					
					}
				stage ('Service start'){
					steps{
							sh "service httpd start"
						}
					}
				
				stage ('Deployment of index.html'){
					steps{
					
							sh "cp -r /mnt/Assignment1/index.html /var/www/html/"
							sh "chmod -R 777 /var/www/html/index.html"
						}
					}
			}
		
	}
}
