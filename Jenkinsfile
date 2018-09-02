node ('slave') {
  
  stage ('Checkout') {
    checkout scm
  }
  // Has a stage ‘build’ executing ‘mvn build’
  stage ('Build') {
    def mvnHome = tool 'M3'
    sh '${mvnHome}/bin/mvn build'
  }
  //Has a stage 'test' excuting 'mvn test'
  stage ('Test') {
    def mvnHome = tool 'M3'
    sh '${mvnHome}/bin/mvn test'
  }

}
