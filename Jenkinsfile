pipeline {
    agent any

    stages {
        stage('first_query') {
            steps {
                sh(script:'''
         
               mysql --user rfamro --host mysql-rfam-public.ebi.ac.uk --port 4497 --database Rfam && SELECT fr.rfam_acc, fr.rfamseq_acc, fr.seq_start, fr.seq_end
FROM full_region fr, rfamseq rf, taxonomy tx
WHERE rf.ncbi_id = tx.ncbi_id
AND fr.rfamseq_acc = rf.rfamseq_acc
AND tx.ncbi_id = 10116 -- NCBI taxonomy id of Rattus norvegicus
AND is_signiÕcant = 1 -- exclude low-scoring
               
               ''')
          
            }
        }
    }
}
