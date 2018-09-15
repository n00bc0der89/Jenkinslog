pipeline {

 agent any
 
 stages {
 
 stage('Get build details'){
    steps {
      echo "Running ${env.BUILD_ID} with name ${env.BUILD_NAME} on ${env.JENKINS_URL}"
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
