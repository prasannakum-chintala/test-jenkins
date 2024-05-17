pipeline {
  agent any
  environment {
    MY_VERSION = '1.0.0'
  }
  parameters {
    booleanParam(name: 'executeTests', defaultValue: false)
    string(name: 'publish', defaultValue: false)
    choice(name: 'version', defaultValue: '2.0.0', choices: ['1.0.0', '2.0.0', '3.0.0'])
  } 
  stages {
      stage("build") {
           steps {
               echo 'Building'
               echo "Version from environment is ${MY_VERSION}"
               withCredentials([usernamePassword(credentialsId: 'mygithubcred', passwordVariable: 'password', usernameVariable: 'username')]){
                  echo "user name is ${username}"
                  echo "password is ${password}"
               } 
               echo "version from parameter is  ${params.version}"
               
             
           }
        
      }
      stage("test") {
           when {
             expression {
                  params.executeTests == true
             }
           }
           steps {
               echo 'Testing'
             
           }
        
      }
      stage("publish") {
           steps {
               echo 'publish value from param is ${params.publish}'
             
           }
        
      }
    
  }

}  
