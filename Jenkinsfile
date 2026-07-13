pipeline{
    agent any
     stages{
        stage('pull'){
          steps{
            sh ' echo "hello this is the pull request"'
          }
        }
       stage('build'){
         steps{
           sh 'echo "hello this is the build request"'
         }
       }
      stage('Test'){
        steps{
          sh 'echo "hello this is the test request"'
        }
      }     
   }
}
