node ('slave1') {
  environment {
        mvnHome = tool('M3')
    }
  stage ('Checkout') {
    checkout scm
  }
  // Has a stage ‘build’ executing ‘mvn build’
  stage ('Build') {
    sh '{env.mvnHome}/bin/mvn build'
  }
  //Has a stage 'test' excuting 'mvn test'
  stage ('Test') {
    sh '{env.mvnHome}/bin/mvn test'
  }

}
