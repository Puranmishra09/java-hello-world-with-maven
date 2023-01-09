pipeline{
    agent any

    tools {
         maven "3.6.3"
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
