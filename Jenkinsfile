pipeline {
    agent any

    stages {
        stage('first_query') {
            steps {
         
                mysql '--user rfamro --host mysql-rfam-public.ebi.ac.uk --port 4497 --database Rfam'
          
            }
        }
    }
}
