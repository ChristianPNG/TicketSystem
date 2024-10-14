pipeline {
  agent {
    docker {
      image 'mcr.microsoft.com/dotnet/sdk:6.0'
      args '-u root'
    }

  }
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/ChristianPNG/TicketSystem.git', branch: 'Jenkins-Testing', credentialsId: '7e52c2f2-55b2-4886-b6bb-e6ef09af4b45')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'dotnet restore'
      }
    }

  }
}