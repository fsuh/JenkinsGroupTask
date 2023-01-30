pipeline {
  agent any

  stages {

    stage ("build") {
      steps {
        sh "npm install"
      }
    }

    stage ("test") {
      steps {
        echo 'testing our app...'
      }
    }

    stage ("deploy") {
        when {
            expression{
                currentBuild.result == null || currentBuild.result == "SUCCESS"
            }
        }
      steps {
        sh "make publish"
      }
    }

  }

}