node {
 def app
 def appversion

 stage('Clone repo') {
   checkout scm
 }

 stage('BUild docker image'){
   app = docker.build("scn3089/node_from_pipeline")
 }

 stage('Run docker image'){
  docker.image("docker/node_from_pipeline").withRun(){
  }
 }
 stage('Generate version'){
 script {
   BUILD_VERSION_GENERATED = VersionNumber(
        versionNumberString: '1.0.0.${BUILDS_ALL_TIME, X}',
        projectStartDate:    '2018-09-17',
        skipFailedBuilds:    true)
    appversion = BUILD_VERSION_GENERATED
    echo "Version number ${appversion}"
 }
 }
 
 stage('Push image')
 {
  docker.withRegistry('https://registry.hub.docker.com','docker-hub') {
   app.push("$appversion");
  }
 }
 



}
