pipeline {
  agent any
  stages {
    stage('Snapshot Build & Deploy') {
      tools {
        jdk 'jdk8'
      }
      environment {
        JAVA_HOME = '/usr/lib/jvm/java-1.8.0-openjdk-amd64'
      }
      steps {
        echo 'Start Update of Central p2 Repository ...'
        sh 'mvn --version'
        sh 'mvn clean install -P p2Deploy -f eclipseProjects/de.enflexit.p2'
        echo 'Finished Update of Central p2 Repository!'
      }
    }

  }
}