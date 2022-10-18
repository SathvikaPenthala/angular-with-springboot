pipeline {
    agent any
    stages {
        stage('git Branch') {
          steps{
           git branch :'master', url: 'git@github.com:SathvikaPenthala/angular-with-springboot.git'
          }
        }
         stage('npm install node module') {
          steps{
           sh 'inpm install'
          }
        }
        stage('buil') {
          steps{
           sh 'inpm run build:ssr'
          }
        }
          stage('Deploye ') {
          steps{
           sh 'pm2 restart all'
          }
        }
        stage('mvn test') {
          steps{
           sh 'mvn test'
          }
        }
    }
}
