// pipeline{
// agent any
// stages{
// stage('Build'){
// steps{
// echo 'Starting the Build Stage'
// }
// }

// stage('Test'){
// steps{
// echo 'Starting the Test Stage'
// }
// }



// stage('Deploy'){
// steps{
// echo 'Starting the Deploy Stage'
// }
// }
// }
// }
node{
  stage('SCM Checkout'){
    git 'https://github.com/kamini-shrivastava/SpringBoot'
  }
  stage('Compile-Package'){
    // Get maven home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    bat "${mvnHome}/bin/mvn package"
  }
}
