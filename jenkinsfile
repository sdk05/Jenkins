pipeline {
    agent any
    tools {
        maven 'Maven-3.9.9'  // Make sure this matches the name configured in Global Tool Configuration
    }
    stages {
        stage("CleanUp"){
            steps {
                deleteDir()
            }
        }
        stage("clone repo"){
            steps{
                sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
            }
        }
        stage ("Build"){
            steps{
                sh "mvn -v"
                dir("simple-java-maven-app"){
            
                    sh "mvn clean install"
                }
            }
        }
        stage ("Test"){
            steps{
                dir("simple-java-maven-app"){
                sh "mvn clean install"
                }

            }
        }
    }

}
