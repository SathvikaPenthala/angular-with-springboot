pipeline {
    agent any
    tools{
        node js '18.11.0'
    }
    stages {
        stage('git Branch') {
          steps{
           git branch :'master', url: 'git@github.com:SathvikaPenthala/angular-with-springboot.git'
          }
        }
         stage('npm install node module') {
          steps{
           sh 'npm install'
          }
        }
      
        stage('mvn test') {
          steps{
           sh 'mvn test'
          }
        }
    }
}
