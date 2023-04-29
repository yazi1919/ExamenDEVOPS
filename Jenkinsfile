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
		
		 post {
        always {
          junit 'target/surefire-reports/*.xml'
        }
			 
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
	    
	    
//stage('SonarQube') {
           // steps {
		  //  dir('Exam'){     sh 'mvn sonar:sonar -Dsonar.login=tokentoken -Dsonar.password=squ_6cfff00a7eebd04b3daeb453aabb8e74efe9dfe7'          }
       //     }
   //     }
  
 
	    
	    stage('Nexus') {
            steps {
                junit 'target/surefire-reports/*.xml'
                nexusArtifactUploader(
                    nexusVersion: 'nexus3',
                    protocol: 'http',
                    nexusUrl: 'http://192.168.122.10:8081/',
                    groupId: 'com.example',
                    version: '1.0-SNAPSHOT',
                    repository: 'maven-releases',
                    credentialsId: 'nexus-credentials',
                    artifacts: [
                        [artifactId: 'example', classifier: 'sources', file: 'target/example-1.0-SNAPSHOT-sources.jar', type: 'jar'],
                        [artifactId: 'example', classifier: 'javadoc', file: 'target/example-1.0-SNAPSHOT-javadoc.jar', type: 'jar'],
                        [artifactId: 'example', file: 'target/example-1.0-SNAPSHOT.jar', type: 'jar']
                    ]
                )
            }
        }
	    
	    
	    
	    
	    
    }
}
