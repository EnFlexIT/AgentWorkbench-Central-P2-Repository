pipeline {
  agent any
  stages {
    stage('Snapshot Build & Deploy') {
      steps {
        echo 'Start Update of Central p2 Repository ...'
        sh 'mvn --version'
        sh 'mvn clean install -P p2DeployClean -f eclipseProjects/de.enflexit.p2'
        echo 'Finished Update of Central p2 Repository!'
      }
    }

  }
}