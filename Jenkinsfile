pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        checkout scm
      }
    }

    stage('Compile') {
      steps {
        mail(subject: 'test', body: 'c\'est un test', to: 'dominique.antoine.raz@gmail.com')
      }
    }

  }
  environment {
    NEXUS_VERSION = 'nexus3'
    NEXUS_PROTOCOL = 'http'
    NEXUS_URL = 'ec2-52-212-29-159.eu-west-1.compute.amazonaws.com:8081'
    NEXUS_REPOSITORY = 'maven-snapshots'
    NEXUS_CREDENTIAL_ID = 'nexus-credentials'
    SONARQUBE_URL = 'http://192.168.99.100'
    SONARQUBE_PORT = '9000'
  }
  options {
    skipDefaultCheckout()
  }
}