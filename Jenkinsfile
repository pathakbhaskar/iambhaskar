pipeline {
  agent any
  stages {
    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
        sh 'sudo service apache2 start'
      }
    }

    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/pathakbhaskar/iambhaskar.git', branch: 'main')
      }
    }

    stage('Deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
        sh 'sudo service apache2 restart'
      }
    }

  }
}