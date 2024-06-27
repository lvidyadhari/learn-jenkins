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
        timeout(time: 1 , unit: 'HOURS')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                  sleep 10
                  """
        }
      } 
        stage('check params'){
            steps{
                sh """
                echo "Hello ${params.PERSON}"


                echo "Toggle: ${params.TOGGLE}"
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