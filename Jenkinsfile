pipeline {
  agent any

  stages {

    stage ("build") {
      steps {
        sh "npm install"
        sh "npm run build"
      }
    }

    stage ("test") {
      steps {
        sh "npm test"
      }
    }

    stage ("deploy") {
      steps {
        sh "cp -r ${WORKSPACE}/build/ /var/www/jenksins-react-app/"
      }
    }

  }

}