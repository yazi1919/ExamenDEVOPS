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

	    
	    stage('SonarQube analysis') {
      steps {
        // Configure SonarQube server details
        withSonarQubeEnv('SonarQube Server') {
          // Run SonarQube analysis
          sh 'mvn sonar:sonar'
        }
      }
    }
      

		
    }
}
