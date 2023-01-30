pipeline {
  agent any

  stages {

    stage ("build") {
      steps {
        sh 'sudo npm install'
        sh 'sudo npm run build'
      }
    }

    stage ("test") {
      steps {
        sh 'sudo npm test'
      }
    }

    stage ("deploy") {
      steps {
        sh "sudo cp -r ${WORKSPACE}/build/ /var/www/jenksins-react-app/"
      }
    }

  }

}