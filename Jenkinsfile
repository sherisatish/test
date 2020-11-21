pipeline {

agent any
    
    stages{
    
        stage("compile stage") {
            
            steps {
                withmaven(maven : "maven_3.6.3") {
                sh 'mvn clean compile'
                }
            }
        }
        stage("testing stage") {
            
            steps {
                withmaven(maven : "maven_3.6.3"){
                sh 'mvn test' 
                }
            }
        }
        stage("deploying stage") {
            
            steps {
                withmaven(maven : "maven_3.6.3"){
                sh 'mvn deploy'
                }
            }
        }
    }

}
