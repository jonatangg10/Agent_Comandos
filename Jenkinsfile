pipeline {
    // agent any
    agent 'linux'
    
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
