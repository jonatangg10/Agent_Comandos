pipeline {
    agent any
    
    stages {
        
        stage('Clonar Repositorio') {
            agent {
                label 'linux'
            }
            steps {
                sh 'echo "Clonammos el repositorio github : jonatangg10"'
                git 'https://github.com/tu_usuario/tu_repositorio.git'
            }
        }
        
        stage('Construir') {
            agent {
                label 'linux'
            }
            steps {
                sh 'echo "Creamos un proyecto Java con: Maven"'
                sh 'mvn clean package'
            }
        }
        
        stage('Pruebas Unitarias') {
            agent {
                label 'linux'
            }
            steps {
                sh 'echo "Hacemos un test a Maven"'
                sh 'mvn test'
            }
        }
    }
}
