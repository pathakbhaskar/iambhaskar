pipeline {
  agent any
  stages {
    stage('Install Apache') {
      steps {
        sh 'sudo yum install httpd -y'
        sh 'sudo yum service httpd start'
      }
    }

    stage('Deployment') {
      steps {
        sh 'sudo cp * /var/www/html/'
      }
    }

  }
}