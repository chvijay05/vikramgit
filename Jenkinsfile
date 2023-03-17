pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               sh "mvn clean package"
               echo "Building Artifact for project"
               
           }
       }
       stage('Reading branch wise')
       {
       when
       {
       branch "stage*"
       }
       steps
       {
       echo " It is only for stage branch"
       }
       }

       stage('Deploy Code') {
	   when
	   {
	   branch "feature"
	   	   }
          steps {
               sh "mvn tomcat7:deploy"
               echo "Deploying Code"
               
          }
      }
      }
      }
