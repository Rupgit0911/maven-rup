node{
stage('SCM Checkout'){

git 'https://github.com/Rupgit0911/maven-rup'
}
stage('Compile-Package'){
def mvnHome = tool name: 'maven-3.6.3', type: 'maven'
sh "${mvnHome}/bin/mvn package"
}
}
