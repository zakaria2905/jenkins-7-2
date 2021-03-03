pipeline {
    agent any
    
    tools {
        maven 'my-maven-3' 
    }
    
    stages {
    	 
	  stage('Static Code Analysis'){
		  steps {
    		sh "mvn clean verify sonar:sonar -Dsonar.host.url=http://host.docker.internal:9000 -Dsonar.projectName=07-static-code-analysis-sonarqube -Dsonar.projectKey=07-static-code-analysis-sonarqube -Dsonar.projectVersion=$BUILD_NUMBER";
		  }
	  }
    }
  }