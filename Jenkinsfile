pipeline{
    agent any
    stages{
        stage("Create Folder"){
            steps{
                sh "mkdir -p ${env.JOB_NAME}"
            }
        }
        stage("Maven Build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("Code Quality"){
            steps{
                sh 'mvn sonar:sonar'
            }
        }
        stage("Deploy to Nexus"){
            steps{
                sh 'mvn deploy'
            }

        }
    }
}

