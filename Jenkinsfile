pipeline {   //1
    agent {   //2
         node {  //3
            label 'agent-1'
        //customWorkspace '/some/other/path'
        } //3
    } //2
    environment { 
        GREETING = 'Hello Jenkins'
    }
    stages { //4
        stage('Build') { //5
           steps { //6
              echo 'Hello'
           } //6
        } //5
        stage('Test') { //7
            steps { 
              echo 'Hi'  
           }
        } //7
        stage('Deploy') { //8
            steps {
               echo 'Good Morning'
        }
      } //8
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
   //4
} //1