pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            git url: 'https://github.com/mahmoudibra96/k8s-1.git' , branch: 'main' , credentialsId: 'githubtoken'
         }
      }
      stage('Docker Build') {
         steps {
            sh(script: 'docker images -a')
            sh(script: """
               cd k8s-web-hello/
               docker build -t node_app .
               cd ..
            """)
         }
      }
   }
}