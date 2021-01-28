pipeline{
  agent any
  stages{
    stage('SCM Checkout'){
      steps{
        withMaven(maven : 'maven-3.6.3'){
       sh 'mvn clean compile'
        }
      }
    }
    stage('Testing Stage'){
      steps{
       withMaven(maven : 'maven-3.6.3'){
       sh 'mvn clean test'
        }
      }
      stage('Deployment Stage'){
        steps{
        withMaven(maven : 'maven-3.6.3'){
       sh 'mvn deploy'
        }
      }
  }
}
