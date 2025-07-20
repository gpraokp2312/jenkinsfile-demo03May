pipeline{
    
    agent any  
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        
        stage('Checkout code '){
            steps{
                
                git 'https://github.com/gpraokp2312/DevOpsCodeDemo.git'
                
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
                sh 'sudo su scp -o StrictHostKeyChecking=no target/*.war /usr/local/tomcat/webapps/addressbook.war'
              }      
           }     
    }

}
