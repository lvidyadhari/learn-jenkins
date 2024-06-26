pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }
    
    stages {
        stage('Build') { 
            steps {
                echo 'Building'
            }
        }
        stage('Test') { 
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') { 
            steps {
                echo 'Deploying'
            }
        }

        post { 
        always { 
            echo 'I will always say Hello again!'
        }
        
        failure { 
            echo 'This shows when the pipeline is failure'
        }
        success { 
            echo 'This shows when the pipeline is success'
        }
    }
    }
}



