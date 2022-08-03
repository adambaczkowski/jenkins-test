pipeline {                                    
   agent {                                    
    kubernetes {                              
      containerTemplate {                     
        name 'maven'                          
        image 'maven:3.8.1-jdk-8'             
        command 'sleep'                       
        args '99d'                            
      }                                       
    }                                         
  }                                           
  stages{         
      stage('Checkout repo') {                         
        steps {                               
            sh("git clone https://github.com/jabedhasan21/java-hello-world-with-maven.git") 
            sh("cd java-hello-world-with-maven")
        }                                     
    }             
    stage('Build') {                         
        steps {        

            sh("cd java-hello-world-with-maven; mvn clean package")                      
        }                                     
    }                                         
    stage('Test') {                           
        steps {     
             sh("cd java-hello-world-with-maven;mvn clean test")                      
        }                                     
    }              
  }                                           
}
