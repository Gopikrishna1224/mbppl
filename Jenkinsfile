pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
	   sh "mvn clean package"
	   echo "building artifact for project samplewebapp"
	   }
	 }

	 stage('reading branch wise')
	 {
	 when
	 {
	 branch"feature"
	 }
	 steps
	 {
	 echo "it is for feature branch"
	 }
	}

	 stage('Deploy code')
	 {
	 when
	 {
	 branch"master"
	 }
	 steps
	 {
	 sh "mvn tomcat7:deploy"
	 echo "deploying code"
	 }
	 }
	 }
	 }

   

