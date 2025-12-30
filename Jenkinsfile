pipeline {
  agent { label 'linux' }  // can run on either agent1 or agent2
  options { timestamps() }

  stages {
    stage('Info') {
      steps {
        sh '''
          echo "Branch=$BRANCH_NAME"
          echo "Node=$NODE_NAME"
          hostname
          echo "Commit:"
          git rev-parse --short HEAD
        '''
      }
    }
  }
}
