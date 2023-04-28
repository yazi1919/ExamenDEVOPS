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
	    
	
 
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

	    
	    
	    
	    
	    
	    
	    
	    
	    
	    
	    

        stage ('Maven Clean'){
            steps
			{
                sh 'sudo mvn clean'
            }
        }

		stage ('Maven Compile'){
            steps
			{
                sh 'mvn compile'
            }
        }

        stage ('Maven Test'){
            steps
			{
                sh 'mvn test'
            }
        }

		stage('Maven Build'){
            steps
			{
                sh 'mvn package'
            }
        }

		stage ('Maven Install'){
            steps
			{
                sh 'mvn install'
            }
        }
	    
	stage('SCM') {
		steps {
			checkout scm
		}
                }
	    
	    

  
 
	    
    }
}
