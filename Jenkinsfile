pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M399"
    }
    
    stages{
        stage('echo version'){
            steps{
                sh 'echo print maven version'
                sh 'mvn -version'
            }
        }
        stage('Build'){
            steps{
                //git branch: 'main', url: 'https://github.com/Adityapradhan14/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Test'){
            steps{
                    script{
                        for (int i=0;i<60;i++){
                        echo "${i+1}"
                        sleep 1
                    }
                   sh 'mvn test'
                }
            }
        }
        
    }
    
}
