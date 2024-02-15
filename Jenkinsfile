pipeline {
    agent any
    
    stages {

        stage('Impresión de las variables del Build') { 
            agent {
                label 'linux'
            }
            steps {
                echo pwd()
                sh 'printenv'
            }
        }
        
        stage('Clonar Repositorio') { 
            agent {
                label any
            }
            steps {
                sh 'echo "Clonammos el repositorio github : jonatangg10"'
                git branch: 'main', url:'https://github.com/jonatangg10/Agent_Comandos.git'
            }
        }

        
    }
}
