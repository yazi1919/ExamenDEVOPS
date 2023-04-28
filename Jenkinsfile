
pipeline {    agent any    stages {       stage('Clone repository') {          steps {             git 'https://github.com/myuser/myrepo.git'          }       }       stage('Run tests') {          steps {             sh 'ant runTests -Dtest.dir=test'          }       }       stage('Publish test results') {          steps {             junit 'test/TEST-results.xml'          }       }    } }
