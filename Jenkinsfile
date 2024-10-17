pipeline {
  agent {
    docker {
      image 'mcr.microsoft.com/dotnet/sdk:8.0'
      args '-u root'
    }

  }
  stages {
    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}