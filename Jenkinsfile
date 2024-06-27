pipeline {
    agent {
         node {
            label 'agent-1'
        //customWorkspace '/some/other/path'
        }
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
               echo 'Good Morning'
        }
      }
    post { 
       always { 
            echo 'I will always say Hello again!'
        }
       failure {
        echo 'I show the message of failure'
       }
       success {
        echo 'I show the message of success'
       }
    }
  }
}