//Start the pipeline 
pipeline{

    //Where the pipeline job will run

    agent {
        label "Windows_Save_01"
    }

    
    //Start of the stages: build, test,deploy ...

    stages{

    
        //Start of the Build stage

        stage('build'){

            
            //Start of the steps to run inside the Build stage

            steps{

            
                //Build with Maven

                bat 'mvn clean install'

            }
            
            stage('deploy') {
             
                steps{
                bat 'sc stop Tomcat7'
                    bat 'ping 127.0.01 -n 6'
                    bat 'xcopy /y "C:\\Program Files (x86)\\CICD\\Jenkins_Slave\\workspace\\GOL_Pipeline\\gameoflife-web\\target\\gameoflife.war"
                    "C:\\Program Files (x86)\\CICD\\Tomcat 7.0\\webapps"'
                    bat 'sc start Tomcat7'
                }
            }

        }

    }
}
