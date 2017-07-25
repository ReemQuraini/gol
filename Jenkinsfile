//Start the pipeline 
pipeline{

    //Where the pipeline job will run

    agent any

    
    //Start of the stages: build, test,deploy ...

    stages{

    
        //Start of the Build stage

        stage('build'){

            
            //Start of the steps to run inside the Build stage

            steps{

            
                //Build with Maven

                bat 'mvn clean install'

            }

        }

    }
}