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
          sh 'git clone https://github.com/Low-Income-Benefits/Pregnanacy-payment-scheme.git'
          sh 'mvn clean'
          sh 'mvn compile'
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
