
pipeline {
    agent {
            label 'wind-node'
          } 
    stages {
        stage('clean') { 
            steps {
                    sh 'rm -rf PipelineCode'
                    sh 'mvn clean -f PipelineCode '
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn test -f PipelineCode'
            } 
        }
        stage('Deploy') { 
            steps {
               sh 'mvn package -f PipelineCode' 
            }
        }
    }
}
