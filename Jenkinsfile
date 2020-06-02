#!groovy

pipeline {
  agent none
  parameters{
    string(name: 'dockerTagName', defaultValue: 'latest', description: 'Docker Tag')
  }
  stages {
    stage('Docker Pull') {
      agent any
      steps {
        sh "docker pull dkulikova/spring-petclinic:${params.dockerTagName}"
      }
    }
    stage('Start container') {
      agent any
      steps {
	sh "docker run -p 8081:8080 dkulikova/spring-petclinic"
      }
    }
  }
}