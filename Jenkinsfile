pipeline {

  agent { node { label 'workplace' } }

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
        sh 'echo welocome to the world'
        echo 'Maneesha Jenkins Learning'
      }
    }
  }

  post {
    always {
      sh 'echo Post'
    }
  }

}
