pipeline {
   agent any
   environment {
         toollused ="Jenkins" 
   }
   // Adding Parameters
   parameters{
     
         booleanParam( name: 'SONAR',          defaultValue: 'true',          description: 'Whether to generate SONAR Reports'          )   
         string(name: 'TOOL' , defaultValue: 'Devops' , description: 'Devops Tool')
         choice(        name: 'myParameter',         choices: "Option1\nOption2",         description: 'interesting stuff' )
      
   }
   //options
   options {
   // Want to retry Build if failed
     // retry(2)
    // Deleting Old Build logs  
      buildDiscarder(logRotator(numToKeepStr:'8'))
      disableConcurrentBuilds()
      // Adding Timeout for builds
      timeout(time:10 , unit:'MINUTES')
   }

   stages {
      
      
      stage('Build Application') {
         // For running commands on windows we use bat --example bat "cd"
         
         steps {
            echo '-----------------Building Application-------------------'
            // Predefined Variables we can see at localhost:8080/env-vars.html
            // Single quotes will not print env variable value 
            echo 'Build details in single quotes are : Build Number $BUILD_NUMBER'
            // Duoble quotes will  print env variable value 
            echo "Build details in Duoble quotes are : Build Number $BUILD_NUMBER  , $toollused,${params.SONAR},${params.myParameter}"
            
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
