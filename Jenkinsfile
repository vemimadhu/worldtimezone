pipeline
	{
	agent any
		stages{
			stage('Build Application'){
				steps{
					bat 'mvn clean install'
				}	
			}
			
			stage('Deploy Application To MuleSoft Cloudhub'){
				steps{
					bat 'mvn package deploy -DmuleDeploy'
				}
			}
			
			stage('Perform Regression Testing'){
				steps{
					bat 'C:\\Users\\biztalkdev\\AppData\\Roaming\\npm\\newman run D:\\newman\\WorldTime.postman_collection.json --disable-unicode'
				}	
			}
		}
	}