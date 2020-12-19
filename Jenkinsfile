pipeline {
	agent any
	tools {
    	   maven 'MAVEN3.6'
	}
	stages {
    	stage("Checkout") {   
        	steps {      
               	    git branch: 'main',url: 'https://github.com/wjfrelo/maven-build-pipeline.git'
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
