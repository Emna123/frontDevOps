pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }

  post {
    failure {
      mail to: 'emnatijani77@gmail.com',
           subject: 'Construction échouée',
           body: 'La construction de votre projet a échoué.'
    }
  }
}
