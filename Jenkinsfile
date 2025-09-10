pipeline {
  agent any

  tools {
    maven '3.9.9'
  }
  
  stages{
    stage("build"){
      steps{
        echo 'step 1 - compile app'
        sh 'mv compile'
      }
    }

    stage("test"){
      steps{
        echo 'step 2 run test'
        sh 'mv clean test'
      }
    }

    stage("package"){
      steps{
        echo 'step 3 package app'
        sh 'mv package -DskipTests'
      }
    }
  }

  post {
    always{
      echo 'Done'
    }
  }
}
