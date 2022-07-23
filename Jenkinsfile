pipeline {
  agent any
  tools {
     maven "my_maven"
	 buildInfo = Artifactory.newBuildInfo()
	 
  }

  stages {
    stage("GIT Checkout") {
      steps {
	    git url: "https://github.com/ssoella/pg-proj1jenkins.git"
	  }
	 
    }
	
	stage("Build") {
	  steps {
	    sh "mvn compile"
	  }
		
	}
	
	}
    stage("SonarQube Analysis") {
      def scannerHome = tool "my_sonarqube";
      withSonarQubeEnv() {
        sh "${scannerHome}/bin/sonar-scanner"
      }
    }
	 
}
	

