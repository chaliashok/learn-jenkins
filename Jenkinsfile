pipeline {

  agent { node { label 'workstation' } }

  environment {
    SSH = credentials('SSH')
    DEMO_URL = "google.com"
  }

  options {
    ansiColor('xterm')
  }

  parameters {
    string(name: 'APP_INPUT', defaultValue: '', description: 'Just Input')
  }

    stages {
    stage('Hello-1') {
      steps {
        echo 'Hello World'
        sh 'env'
        sh 'echo APP_INPUT - $APP_INPUT'
      }
    }
  }

  post {
    always {
      sh 'echo Post'
    }
  }

}
