  pipeline {
    agent { node { label 'workplace' } }
    environment {
       SSH = credentials('SSH')
       DEMO_URL = "google.com"
     }
    stages {
        stage('hello-1') {
            steps {
                echo "hello world"
                sh 'env'
            }
        }
    }
  }