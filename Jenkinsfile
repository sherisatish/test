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
                sh 'mvn archetype:generate -DarchetypeGroupId=com.insurance -DarchetypeArtifactId=loanone -DarchetypeVersion=1.0.0-SNAPSHOT -DgroupId=Reloader -DartifactId=Reloader -Dversion=1 -e'
                
            }
        }
    }

}
