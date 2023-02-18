pipeline{
  agent any
    stages {
      stage('Build') {
        steps {
          sh 'g++ -o pes2ug20cs490-1 pes2ug20cs490.cpp'
          echo 'Build Success!' 
        }
      }
      stage('Test'){
        steps {
          sh './pes2ug20cs490-1'
          echo 'Test Success!'
        }
      }
      stage('Deploy'){
        steps{
           echo 'Deployment Success!'
        }
      }
    }
    post
    {
      failure{
        echo 'Pipeline failed'
      }
    }
  }
