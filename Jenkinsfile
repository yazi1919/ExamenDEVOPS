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
                sh 'mvn clean'
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

        stage('Test') {
            steps {
                sh 'docker run myapp mvn test'
            }
            post {
                always {
                junit 'target/surefire-reports/*.xml'
                }
            }
    }
    }
}
