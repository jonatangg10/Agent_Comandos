pipeline {
    agent any
    
    stages {

        
        stage('Clonar Repositorio') {
            agent {
                label 'linux'
            }
            steps {
                sh 'echo "Clonammos el repositorio github : jonatangg10"'
                git 'https://github.com/jonatangg10/Agent_Comandos.git'
            }
        }

        
    }
}
