pipeline{
    agent any

    tools {
         maven "maven-3"
         }
    stages{
         stage('build'){
            steps{
               sh "mvn clean package -DskipTests=true"
               archive 'target/*.jar'
            }
        }
    }
     stages{
         stage('test'){
            steps{
               sh "mvn test"
               }
            post{
                always{
                    junit 'target/surefire-reports/*.xml'
                 }
             }
         }
     }
}
