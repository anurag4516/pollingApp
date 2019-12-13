pipeline {
   agent any

   stages {
      
      
      stage('Build Application') {
         // For running commands on windows we use bat --example bat "cd"
         
         steps {
            echo '-----------------Building Application-------------------'
            // Predefined Variables we can see at localhost:8080/env-vars.html
            // Single quotes will not print env variable value 
            echo 'Build details in single quotes are : Build Number $BUILD_NUMBER'
            // Duoble quotes will  print env variable value 
             echo "Build details in Duoble quotes are : Build Number $BUILD_NUMBER"
            
         }
      }
      
      stage('Test Application') {
         steps {
            echo '-----------------Testing Application-------------------'
            echo '-------------Running Automated Test -----'
            echo ' ----------- Analysing Results -----------'
         }
      }
      
      stage('Dockerizing Application') {
         steps {
            echo '-----------------dockerizing Application-------------------'
            
         }
      }
      
            stage('Deploy Application') {
         steps {
            echo '-----------------Deploying Application-------------------'
            
         }
      }
      
      
      
      
      
   }
}
