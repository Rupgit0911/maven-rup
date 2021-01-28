pipeline{
  agent any
  stages{
    stage('SCM Checkout'){
      steps{
      git 'https://github.com/Rupgit0911/maven-rup'
        withMaven(maven : 'maven-3.6.3'){
       sh 'mvn clean compile'
        }
      }
    }
    stage('Testing Stage'){
      steps{
      git 'https://github.com/Rupgit0911/maven-rup'
       withMaven(maven : 'maven-3.6.3'){
       sh 'mvn clean test'
        }
      }
      stage('Deployment Stage'){
        steps{
      git 'https://github.com/Rupgit0911/maven-rup'
        withMaven(maven : 'maven-3.6.3'){
       sh 'mvn deploy'
        }
      }
  }
}
