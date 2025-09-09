pipeline {
  agent any
  stages{
      stage("build"){
          steps{
              echo 'maven compile sysfoo app..'
              sh 'maven compile'
          }
      }
      stage("test"){
          steps{
              echo 'test maven app'
             sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'package maven app'
              mvn package -DskipTests
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
