pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '/var/jenkins_home/opt/apache-maven-3.6.2/bin/mvn -B -DskipTests clean package'
      }
    }
    stage('test') {
      steps {
        sh '/var/jenkins_home/opt/apache-maven-3.6.2/bin/mvn test'
      }
    }
  }
}