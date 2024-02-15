pipeline {
    agent any
    
    stages {
        

        
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
