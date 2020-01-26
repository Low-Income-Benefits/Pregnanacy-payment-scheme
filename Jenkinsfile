#! /Groovy

pipeline {
  agent any
  stages {
    stage('Clean'){
      echo 'Deleting Workspace'
      deleteDir()
      }
    stage('Checkout'){
      checkout scm
      }
    stage('Compile'){
      script{
      sh 'mvn clean compile'
      }
      }
    stage('Test'){
      script {
      sh 'mvn test'
      }
      }
    stage('Build'){
    script {
    sh 'mvn package'
    }
    }
    }
    }
