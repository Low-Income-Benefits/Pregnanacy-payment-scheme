#! /Groovy

pipeline {
  agent any
  stages {
    stage('Clean'){
      steps{
      echo 'Deleting Workspace'
      deleteDir()
      }
      }
    stage('Checkout'){
      steps{
        checkout scm
      }
    }
    stage('Compile'){
      steps{
        script{
          sh 'mvn clean compile'
      }
      }
    }
    stage('Test'){
      steps{
        script {
          sh 'mvn test'
       }
      }
      }
    stage('Build'){
      steps{
        script {
          sh 'mvn package'
    }
    }
    }
    }
    }
