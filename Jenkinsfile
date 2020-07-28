
node {
   // This is to demo github action	
   // def sonarUrl = 'sonar.host.url=http://172.31.30.136:9000'
   def mvn = tool (name: 'maven-3', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master', 
	credentialsId: 'github', 
	url: 'https://github.com/javahometech/myweb'
   
   }
   
    
	
   stage('Mvn Package'){
	   // Build using maven
	   
	   sh "${mvn} clean package deploy"
   }
   
   stage('deploy-dev'){
       
          echo "Running the integration test..."
         
	  
   }
  
}

