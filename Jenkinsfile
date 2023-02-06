pipeline {
  agent any
  
  tools {nodeJs ('node')}

  stages {

    stage ("build") {
      steps {
        sh "npm install"
        sh "npm run build"
      }
    }

    stage ("test") {
      steps {
        sh "sudo npm test"
      }
    }

    stage ("deploy") {
      steps {
        echo " deployed in AWS"
      }
    }

  }

}