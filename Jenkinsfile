pipeline {
   agent any

   triggers {
       githubPush()
   }

   stages {
      stage('Build & Deploy'){
         steps {
            sh'''
            docker-compose down || true
            docker-compose up -d  --build
            '''
         }
      }
   }
}
 
