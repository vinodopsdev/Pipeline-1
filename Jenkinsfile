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
        stage("Deploy to Tomcat Dev"){
            steps{
                sh 'mvn tomcat7:deploy'
            }

        }
    }
}

