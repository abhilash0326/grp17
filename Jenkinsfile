pipeline{
			agent {
					label{ 
						label 'Slave-2'
						customWorkspace '/data/22Q2'
							}
			}
		stages{
	
				stage('install apache'){
				
					steps{
							sh "rm -rf /var/www/html/index.html"
							sh "yum install httpd -y"
					
					}
				}
				stage ('Service start'){
					steps{
							sh "service httpd start"
						}
					}
				
				stage ('Deployment of index.html'){
					steps{
					
							sh "cp -r /data/22Q2/index.html /var/www/html/"
							sh "chmod -R 777 /var/www/html/index.html"
						}
					}
			}
}

