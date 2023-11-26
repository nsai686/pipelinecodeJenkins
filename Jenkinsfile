pipeline{
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        
        stage('Clone Repo'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        
        stage('Compile code'){
            steps{
                
                sh 'mvn compile'
            }
        }
         stage('Code Review'){
            steps{
                
                sh 'mvn pmd:pmd'
            }
        }
        
         stage('Code Test'){
            steps{
                
                sh 'mvn test'
            }
        }
        
        stage('Code Build'){
            steps{
            
                sh 'mvn package'
            }
        }
        
    }
}
