pipeline {
    agent any
    options {
    skipDefaultCheckout(true)
     }
    stages {

    stage('However I want to name a stage') {
        steps {
            checkout scm
            }
            }
        // stage('Clone sources') {
        //     steps {
                
        //         git url: 'https://github.com/kloud9nyc/pyspark-unit-testing.git/'

        //     }
        // }
        stage('TEST'){
            steps{
                sh """
                cd /Users/DK/.jenkins/
                ls -lh
                cd /Users/DK/.jenkins/workspace
                ls -lh
                cd && mkdir -p summa-jenkins
                cd
                ls -lh
                pwd
                ls -lh
                cd /Users/DK/.jenkins/workspace/test
                ls -lh
                cd ${WORKSPACE}
                pwd
                ls -lh
                
                  ls -lh /Users/DK/.jenkins/workspace
                  ls -lh /Users/DK/.jenkins/workspace/test/
                 """
            }
        }
        stage('ENV values') {
            steps {
                sh """
               
                    echo $WORKSPACE
                    echo $BUILD_ID
                    cd ${WORKSPACE}
                    ls -lh
                
                
                """
            }
        }
    
    
        
        stage('Download S3 json') {
            steps {
                
                git url: 'https://github.com/kloud9nyc/pyspark-unit-testing.git/'
                sh """
                cd
                mkdir  -p text
                ls -l|grep text
                pwd
                echo $WORKSPACE
                cp ${WORKSPACE}/src/a.txt /Users/DK/text/
                ls -lh /Users/DK/text
                """

            }
        }
         stage('IP config') {
            steps {
                sh """
               
                    printenv|sort
                
                
                
                """
            }
        }
    }
   
}
