pipeline {
   agent any /*{
      docker {image 'node:8.5.0'} 
   }  */
   /*
   environment {
      GLOBAL_JEAN='Jean Paul Drlik'
   }
   */
   
   parameters {
      string(name: 'DEPLOYER', defaultValue: 'Mr Jenkins', description: 'Who are you?')
      choice(name: 'DEPLOY_TO', choices: 'development\nproduction', description: 'Deploy to...')      
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
      stage('Deploy PROD') {
         steps {
            timeout(time:1, unit:'DAYS'){
               input message: 'Are you sure?'
            }
            sshagent (credentials: ['servidor-treinamento']) {
               sh 'ssh -o StrictHostKeyChecking=no ubuntu@172.31.9.116 "ls -al"'
            }
            echo 'Deploying and connecting to remote hots.......'
         }
      }
   }
}
