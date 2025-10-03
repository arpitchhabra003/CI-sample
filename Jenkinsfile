pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout([$class: 'GitSCM',
          branches: [[name: 'refs/heads/main']],
          userRemoteConfigs: [[url: 'https://github.com/arpitchhabra003/CI-sample.git', credentialsId: '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
']]
        ])
      }
    }
  }
}
