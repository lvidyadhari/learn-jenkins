pipeline {   
    agent {   
         node {  
            label 'agent-1'
        //customWorkspace '/some/other/path'
        } 
    } 
    environment { 
        GREETING = 'Hello Jenkins'
    }
    options {
        timeout(time: 1;unit: 'HOURS')
    }
    stages { 
        stage('Build') { 
           steps { 
              echo 'Hello'
           } 
        } 
        stage('Test') { 
            steps { 
              echo 'Hi'  
           }
        } 
        stage('Deploy') { 
            steps {
               sh """
                  echo "Here I wrote shellscript"
                  echo "$GREETING"
                  sleep = 10
                  """
        }
      } 
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'I will show a failure message'
        }
        success {
            echo 'I will show a success message'
        }
     
    }
   //4
} //1