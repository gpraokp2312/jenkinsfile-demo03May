pipeline{
    
    agent any  
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        
        stage('Checkout code '){
            steps{
                
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
                
            }
        }
        
         stage('compile code '){
            steps{
                
                sh 'mvn compile'
                
            }
        }
        
        stage('Test code '){
            steps{
                sh 'mvn test'
            }
        }
        
        stage('Package code '){
            steps{
                
                sh 'mvn package'
                
            }
        }

        stage ('Deploy-To-Tomcat') {
            steps {
                sh 'sudo scp -o StrictHostKeyChecking=no target/*.war root@ip-172-31-44-38:/usr/local/tomcat/webapps/addressbook.war'
              }      
           }       
    }

}
