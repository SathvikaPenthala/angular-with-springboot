pipeline {
    agent any
    stages {
        stage('git Branch') {
          steps{
           git branch :'master', url: 'git@github.com:SathvikaPenthala/angular-with-springboot.git'
          }
        }
        
        stage('mvn test') {
          steps{
           sh 'mvn test'
          }
        }
    }
}
