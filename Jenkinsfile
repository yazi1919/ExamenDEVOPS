pipeline {


    agent any
	
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
		     mvnHome = tool 'M2_HOME'
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
    }
}
