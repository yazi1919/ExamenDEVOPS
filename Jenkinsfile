pipeline {


    agent any
	
	    
	 environment {
        JAVA_HOME = "/usr/bin/java"
    }
	
 tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M2_HOME"
    }

    stages {

        stage("Cloning Project"){
            steps {
                git branch: 'main',
                url: 'https://github.com/yazi1919/ExamenDEVOPS.git'
                echo 'checkout stage'
		 
            }
        }
	    
	
 
   
	    
	    
	    
	    
	    
	    
	    
	    
	    
	    
	    

        stage ('Maven Clean'){
            steps
			{
				dir('Exam'){   sh 'sudo mvn clean'}
            }
        }

		stage ('Maven Compile'){
            steps
			{
				dir('Exam') {sh 'mvn compile'}
            }
        }

        stage ('Maven Test'){
            steps
			{
				dir('Exam'){ sh 'mvn test'}
            }
        }

		stage('Maven Build'){
            steps
			{
				dir('Exam') { sh 'mvn package'}
            }
        }

		stage ('Maven Install'){
            steps
			{
				dir('Exam'){ sh 'mvn install'}
            }
        }
	    
	stage('SCM') {
		steps {
			checkout scm
		}
                }
	    
	    

  
 
	    
    }
}
