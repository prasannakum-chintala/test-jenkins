pipeline {
  agent any
  environment {
    MY_VERSION = '1.0.0'
  }
  stages {
      stage("build") {
           steps {
               echo 'Building'
               echo "Branch name for the current VERSION is ${MY_VERSION}"
             
           }
        
      }
      stage("test") {
           steps {
               echo 'Testing'
             
           }
        
      }
      stage("deploy") {
           steps {
               echo 'Deploying'
             
           }
        
      }
    
  }

}  
