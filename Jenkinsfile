pipeline {
  agent any
  stages {
    stage('Snapshot Build & Deploy for Java 21') {
      steps {
        echo 'Start updating central p2 repository ...'
        sh 'mvn --version'
        sh 'mvn clean install -P p2Deploy -f eclipseProjects/de.enflexit.p2 -Dtycho.localArtifacts=ignore -Dtycho.localArtifacts=ignore -Dtycho.p2.transport.min-cache-minutes=0'
        echo 'Finished update of central p2 repository!'
      }
    }

  }
}