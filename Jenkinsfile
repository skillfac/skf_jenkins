pipeline {
    agent any

    stages {
        stage('first_query') {
            steps {
                sh(script:'''
         
               mysql --user rfamro --host mysql-rfam-public.ebi.ac.uk --port 4497 --database Rfam -e "select * from fr.fram_acc limit 1;"
               
               ''')
          
            }
        }
    }
}
