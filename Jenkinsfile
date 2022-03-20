pipeline {
   agent any
     stages {
        stage('Build Code') {
	steps {
	    sh "mvn clean package"
	    echo "building Artifact for project samplewebapp"


	  }

	}
	stage ('Reading branch wise')
	{
	when
	{
	branch "stage"
	}
	steps
	{
	echo "It is only for stage branch"
	}
	}

	stage('Deploy Code') {
	when
	{
	branch "master"
	}
	  steps {
	     sh "mvn tomcat7:deploy"
	     echo "Deploying Code"
	     }


	 }
	 }
	 }
	 
	   
