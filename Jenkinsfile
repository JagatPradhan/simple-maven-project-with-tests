
pipeline {
    ageny any
    stages ('Build Project-J'){

        Steps{
            //Git checkout
            git https://github.com/JagatPradhan/simple-maven-project-with-tests.git
                }
        Steps{
            //For Linux machines only
            sh 'mvn clean package'
        }
        
    }

}
