pipeline{
    
    agent any
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        stage('Checkout Code')
        {
            steps{
                git 'https://github.com/ukm3423/JenkinsProject.git'
            }
        }
        
        stage('ComplileCode'){
            steps{
                echo "Start Compiling Code"
                bat 'mvn compile'
            }
        }
        
        stage('Test Code'){
            steps{
                echo "Start Testing Code"
                bat 'mvn test'
            }
        }
        
        stage('Build Code'){
            steps{
                echo "Start Building Code"
                bat 'mvn clean install package'
            }
        }
    }
    
}
