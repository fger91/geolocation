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
               sh"mvm clean"
               sh"mvm install"
               sh"mvm package"
            
            }
        }
                stage('test') {
            steps {
                 sh"mvm test"
                
            }
        }
                stage('test') {
            steps {
                echo 'test'
                
            }
        }
                stage('deploy') {
            steps {
                echo 'deploy'
                
            }
        }
    }
}