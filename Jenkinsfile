pipeline{
    agent any

    tools {
         maven 
         }
    stages{
         stage('build'){
            steps{
               sh "mvn clean package -DskipTests=true"
               archive 'target/*.jar'
            }
        }
    }
}
