pipeline{
			agent {
					label{ 
						label 'built-in'
						customWorkspace '/data/master'
							}
			}
		stages{
	
				stage('install apache'){
				
					steps{
							sh "rm -rf /var/www/htm/index.html"
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
					
							sh "cp -r /data/master/index.html /var/www/html/"
							sh "chmod -R 777 /var/www/html/index.html"
						}
					}
			}
}

