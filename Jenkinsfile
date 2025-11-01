pipeline {
  agent any
  stages {
    stage('Checkout develop') {
      steps {
        git branch: 'develop', url: 'https://github.com/arindam255064-ux/git_assignment.git'
      }
    }
    stage('Copy to folder') {
      steps {
        sh '''
        TARGET_DIR=/opt/apps/myapp-develop
        sudo rm -rf $TARGET_DIR
        sudo mkdir -p $TARGET_DIR
        sudo cp -r ./* $TARGET_DIR/
        sudo chown -R jenkins:jenkins $TARGET_DIR
        '''
      }
    }
  }
}
