pipeline {
  agent {
    docker {
      image 'bitnami/dotnet-sdk:latest'
    }

  }
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/ChristianPNG/TicketSystem.git', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'sh \'dotnet build\''
      }
    }

  }
}