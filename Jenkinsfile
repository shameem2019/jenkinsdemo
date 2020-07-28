
node {
   // This is to demo github action	
   // def sonarUrl = 'sonar.host.url=http://172.31.30.136:9000'
   def mvn = tool (name: 'maven-3', type: 'maven') + '/bin/mvn'
   stage('SCM Checkout'){
    // Clone repo
	git branch: 'master', 
	//credentialsId: 'github', 
	url: 'https://github.com/shameem2019/jenkinsdemo'
   
   }
   
    
	
   stage('Mvn Package'){
	   // Build using maven
	   
	   sh "${mvn} clean package"
   }
   stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
   }
   
   stage('deploy-dev'){
       
          echo "Running the integration test..."         
	  
   }
  
}

