pipeline {
   agent any /*{
      docker {image 'node:8.5.0'} 
   }  */
   
   environment {
      GLOBAL_JEAN='Jean Paul Drlik'
   }
   
   triggers {
      pollSCM('* * * * *')
   }
   
   stages {
      stage('Build') {
         steps {
            echo 'Building...'
            sh 'pwd'
            sh 'ls -l'
            sh 'df'
            //sh 'node -v'
            sh 'printenv'
         }
      }
      stage('Test') {
         steps {
            echo 'Testing...'
            sh 'cd /tmp'
            sh 'ls -l'
            sh 'cat arquivo-texto3'
         }
      }
      stage('Deploy') {
         steps {
            echo 'Deploying...'
            sh 'cd'
            sh 'pwd'
            sh 'ls -l'
         }
      }
   }
}
