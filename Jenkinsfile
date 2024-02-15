pipeline {
    agent any
    
    stages {
        stage('Etapa de Construcción') {
            agent {
                label 'linux' // Este agente se ejecutará en un nodo etiquetado como 'linux'
            }
            steps {
                // Agrega aquí los pasos de construcción de tu proyecto
                sh 'echo "Construyendo el proyecto en un agente Linux"'
            }
        }
        
        stage('Etapa de Pruebas') {
            agent {
                label 'linux'
            }
            steps {
                // Agrega aquí los pasos de pruebas de tu proyecto
                sh 'echo "Ejecutando pruebas en un agente Linux"'
            }
        }
        
        stage('Etapa de Despliegue') {
            agent {
                label 'linux'
            }
            steps {
                // Agrega aquí los pasos de despliegue de tu proyecto
                sh 'echo "Desplegando el proyecto en un agente Linux"'
            }
        }
    }
}
