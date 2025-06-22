pipeline {
    agent any
 
    stages {
 
        stage(‘cloneproject’) {
            steps {
                git branch:’main’, url:’https://github.com/PraveenKuber/Amazon-Jenkins’
            }
        }
 
        stage(‘clean’) {
            steps {
                sh ‘mvn clean’
            }
        }
 
        stage(‘compile’) {
            steps {
                sh ‘mvn compile’
            }
        }
 
        stage(‘test’) {
            steps {
                sh ‘mvn test’
            }
        }     
 
        stage(‘build’) {
            steps {
                sh ‘mvn clean install’
            }
        }  
   post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

    }
}
