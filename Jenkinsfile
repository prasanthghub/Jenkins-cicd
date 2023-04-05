pipeline {
	agent slave1,slave2
	tools {
    	maven 'my_mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'session5.2_pipeline', url: 'https://github.com/prasanthghub/Jenkins-cicd.git'        	 
           	 
        	}    
    	}
    	stage('clean') {
        	steps {
        	sh "mvn clean"  	 
        	}
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	}
}
}
}
