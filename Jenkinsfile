pipeline {


    agent any
	
	    

	
 
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
				dir('Exam'){   sh 'mvn clean'}
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
