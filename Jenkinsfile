pipeline {
    // agent any
    agent {
        label 'linux'
    }
    
    stages {
        stage('Impresión de las variables del Build') { 
            // agent {
               // label 'linux'
            // }
            steps {
                echo pwd()
                sh 'printenv'
            }
        }
    }
    
}
