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
        
                stage('deploy') {
            steps {
                echo 'deploy'
                
            }
        }
    }
}