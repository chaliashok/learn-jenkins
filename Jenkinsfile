pipeline {

  agent { node { label 'workplace' } }

  environment {
    SSH = credentials('SSH')
    DEMO_URL = "google.com"
  }
  options {
    ansiColor('xterm')
  }

  triggers { pollSCM('H/2 * * * *') }

  parameters {
    string(name: 'APP_INPUT', defaultValue: '', description: 'Just Input')
  }

    stages {
    stage('Hello-1') {
       input {
                    message "Should we continue?"
                    ok "Yes, we should."
                    }
      steps {
        echo 'Hello World'
        sh 'env'
        sh 'echo APP_INPUT - $APP_INPUT'
        sh 'echo welocome to the world'
        echo 'Maneesha Jenkins Learning'
      }
    }
    stage('Example Deploy') {
                when {
                    branch 'production'
                }
                steps {
                    echo 'Deploying'
                }
          }
  }

  post {
    always {
      sh 'echo Post'
    }
  }

}
//commit