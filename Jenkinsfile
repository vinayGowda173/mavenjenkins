pipeline{
  agent any
    tools{
      maven 'Maven'
    }
    stages{
      stage('checkout')
      {
        steps{
          git branch:'master' ,url:'https://github.com/vinayGowda173/mavenjenkins.git'
            }
      }
        stage('build')
        {
          steps{
            sh 'mvn clean install'
          }
        }
      stage('run application')
      {
        steps{
          sh 'java -jar target/mavenjenkins-1.0-SNAPSHOT.jar'
        }
      }
    }

    post
    {
      success{
        echo 'successful'
      }
      failure
      {
        echo 'failure'
      }
    }
  }

      
