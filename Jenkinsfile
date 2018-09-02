node ('slave') {
  def mvnHome = tool 'M3'
  echo mvnHome
  stage ('Checkout') {
    checkout scm
  }
  // Has a stage ‘build’ executing ‘mvn build’
  stage ('Build') { 
    sh "${mvnHome}/bin/mvn compile"
  }
  //Has a stage 'test' excuting 'mvn test'
  stage ('Test') {
    sh "${mvnHome}/bin/mvn test"
  }

}
