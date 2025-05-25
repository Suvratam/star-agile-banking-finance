pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/Suvratam/star-agile-banking-finance.git', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t suvratam/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8085:8081 suvratam/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
