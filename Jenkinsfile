pipeline {
    triggers {
  pollSCM '* * * * *'
  }
    agent any
    tools {
  maven 'M2_HOME'
}
  


        stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
         stage('test') {
            steps {
                mvn 'test'
                
            }
        }
         
         stage('deploy') {
            steps {
                echo 'deploy'
                mvn 'test'
            }
        }
         stage ('Docker') {
             steps {
                 echo 'Image step'
             }
         }
}
