pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            git url: 'https://github.com/mahmoudibra96/k8s-1.git' , branch: 'main' , credentialsId: 'githubtoken'
         }
      }
   }
}