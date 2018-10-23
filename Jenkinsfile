#!groovy

node {
  stage 'Checkout'
    checkout scm

  stage 'Setup'
    sh 'sudo npm install'

  stage 'Mocha test'
    sh 'sudo npm test'

  stage 'Cleanup'
    echo 'Prune and cleanup'
    sh 'sudo npm prune'
    sh 'sudo rm node_modules -rf'
}
