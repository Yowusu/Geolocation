pipeline {
    agent any
    tools {
  maven 'M2_HOME'
}
   triggers {
  pollSCM '* * * * *'
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
         stage('test') {
            steps {
                echo 'test'
                mvn 'test'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy'
                mvn 'test'
            }
        }
    }
}