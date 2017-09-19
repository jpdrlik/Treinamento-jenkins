pipeline {
   agent {
      docker {image 'node:8.5.0'} 
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
            sh 'node -v'
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
