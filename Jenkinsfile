pipeline {
   agent any
   
   stages {
      stage('Build') {
         steps {
            echo 'Building...'
            sh 'pwd'
            sh 'ls -l'
         }
      }
      stage('Test') {
         steps {
            echo 'Testing...'
            sh 'cd /tmp'
            sh 'ls -l'
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
