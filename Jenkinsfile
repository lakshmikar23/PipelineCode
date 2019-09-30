
pipeline {
    agent {
            label 'wind-node'
          } 
    stages {
        stage('clean') { 
            steps {
                    
                    bat 'mvn clean -f PipelineCode '
            }
        }
        stage('Test') { 
            steps {
                bat 'mvn test -f PipelineCode'
            } 
        }
        stage('Deploy') { 
            steps {
               bat 'mvn package -f PipelineCode' 
            }
        }
    }
}
