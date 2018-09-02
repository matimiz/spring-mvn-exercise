#!groovy
node('slave1') {
     stage ('Checkout'){
   checkout scm   
   }
   stage ('Maven Build'){  
      def mvnHome = tool 'maven3'
      sh "${mvnHome}/bin/mvn build"
   }
   stage('test') {
   sh "${mvnHome}/bin/mvn test"
   }
}
