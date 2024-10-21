pipeline {
  agent {
    docker {
      image 'mcr.microsoft.com/dotnet/sdk:8.0'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        sh 'mkdir -p ${DOTNET_CLI_HOME}'
        echo "DOTNET_CLI_HOME is set to: ${env.DOTNET_CLI_HOME}"
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
        sh 'docker build -t ticketingsystem-image .'
      }
    }

  }
  environment {
    DOTNET_CLI_HOME = '/tmp/DOTNET_CLI_HOME'
  }
}