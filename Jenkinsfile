// In google search as jenkins pipeline syntax --> pipeline syntax(jenkins) --> click on pipeline --> copy the code below this Declarative Pipeline fundamentals 
pipeline {
    agent { label 'AGENT-1' }
    environment { 
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND' 
        DEPLOY_TO = 'production'
    }
    options { 
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECONDS') 
    } 
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello, this is build"
                        echo "project: $PROJECT"
                        sleep 15
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Hello, this is test"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                        echo "Hello, this is deploy" 
                    """
                }
            }
        }
    }
    //In google search as jenkins pipeline syntax --> pipeline syntax(jenkins) --> post
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'I will run when pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }    
}