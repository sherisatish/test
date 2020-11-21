pipeline {

agent any
    
    stages{
    
        stage("compile stage") {
            
            steps {
                sh 'mvn clean compile'
                
            }
        }
        stage("testing stage") {
            
            steps {
                sh 'mvn test' 
                
            }
        }
        stage("deploying stage") {
            
            steps {
                sh 'mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
 -Dversion=1 -e'
                
            }
        }
    }

}
