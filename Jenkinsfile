pipeline {

 agent any
 environment{
   DEV="Development"
 }
 
 stages {
 
 stage('Get build details'){
    steps {
      echo "Running build number ${env.BUILD_DISPLAY_NAME} on ${env.JENKINS_URL} in ${env.DEV} environment"
     }
  }   
 stage('Checkout code'){
    steps {
      echo "Checkout code step here"
     }
  }
  stage('Build code'){
    steps {
      echo "Build code"
     }
  }
  stage('Test code'){
    steps {
      echo "Test code here"
     }
  }
  stage('Deploy code'){
    steps {
      echo "Deploy code here"
     }
  }
  
  }
}
