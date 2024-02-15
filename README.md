<p align="center">¡ Bienvenido !</p>
<p align="center"><b>Ejemplo practico de Jenkins</b></p>
<p align="center"><a>Configuración de un <b>Agent</b> y la ejecución de comandos <b>Linux</b></a></p>
<p align="center"><b>Si se puede inmaginar, se puede programar</b></p>

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


