pipeline {
    agent any
    stages {
        stage('git Branch') {
          steps{
           git branch :'master', url: 'git@github.com:SathvikaPenthala/angular-with-springboot.git'
          }
        }
        stages {
    stage('Install') {
      steps { sh 'npm install' }
    }

    stage('Test') {
      parallel {
        stage('Static code analysis') {
            steps { sh 'npm run-script lint' }
        }
        stage('Unit tests') {
            steps { sh 'npm run-script test' }
        }
      }
    }

    stage('Build') {
      steps { sh 'npm run-script build' }
    }
        stage('mvn test') {
          steps{
           sh 'mvn test'
          }
        }
    }
}
