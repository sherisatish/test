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
                sh 'mvn archetype:generate -DgroupId=fr.myGroupId -DartifactId=MyApplication -Dpackagename=fr.myGroupId -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false -Dversion=1 -e'
                
            }
        }
    }

}
