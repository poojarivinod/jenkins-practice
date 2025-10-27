// In google search as jenkins pipeline syntax --> pipeline syntax(jenkins) --> click on pipeline --> copy the code below this Declarative Pipeline fundamentals 
pipeline {
    agent { label 'AGENT-1' }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello, this is build"
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
                        abcd
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