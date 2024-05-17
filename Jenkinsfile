pipeline {
  agent any
  stages {
      stage("build") {
           steps {
               echo 'Building'
               echo "Branch name for the current build is ${BRANCH_NAME}"
             
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
