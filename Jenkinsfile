pipeline {
    agent any 
    
    tools{
        maven 'M3'
    }
    stages {
        
        stage('Compile') { 
            steps {
                // 
                echo 'etape Compile'
                bat 'mvn clean compile'
            }
        }
        
        stage('Test') { 
            steps {
                // 
                echo 'etape Test'
                bat 'mvn clean test'
            }
        }
        stage('Packaging') { 
            steps {
                // 
                echo 'etape Packaging'
                bat 'mvn clean package'
            }
         }
        stage('Deploy') { 
            steps {
                // 
                echo 'etape Deploy'
                copy /y 'C:\opt\Jenkins\workspace\eBureaupipeline\target\ebureau.war' 'C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps\ebureau.war'
                
            }
        }
    }
}
