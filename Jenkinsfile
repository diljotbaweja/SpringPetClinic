pipeline{
    agent any
    tools {maven "m3"}
    stages{
        stage("checkout"){
            steps{
                git branch: "main", url: "https://github.com/diljotbaweja/SpringPetClinic.git"
            }
        }
        stage("build"){
            steps{
                bat "mvn compile"
            }
        }
        stage("test"){
            steps{
                bat "mvn test"
            }
        }
        stage("package"){
            steps{
                bat "mvn package"
            }
        }
        stage("deploy"){
            steps{
                bat "java -jar \"C:/ProgramData/Jenkins/.jenkins/workspace/petClinicDeclarativePipeline/target/spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar\""
            }
        }
    }
}
