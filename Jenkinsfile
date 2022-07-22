pipeline {
  agent any
  tools {
     maven "my_maven"
  }

  stages {
    stage("GIT Checkout") {
      steps {
            git url: "https://github.com/ssoella/pg-proj1jenkins.git"
        }
  }

}

}

