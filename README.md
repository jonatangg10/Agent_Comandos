<p align="center">¡ Bienvenido !</p>
<p align="center"><b>Ejemplo practico de Jenkins</b></p>
<p align="center"><a>Configuración de un <b>Agent</b> y la ejecución de comandos <b>Linux</b></a></p>
<p align="center"><b>Si se puede inmaginar, se puede programar</b></p>


pipeline {
    agent any
    
    stages {
        stage('Clonar Repositorio') {
            steps {
                git 'https://github.com/tu_usuario/tu_repositorio.git'
            }
        }
        
        stage('Construir') {
            steps {
                sh 'mvn clean package'
            }
        }
        
        stage('Pruebas Unitarias') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Desplegar en Servidor Remoto') {
            steps {
                // Supongamos que tu artefacto es un archivo JAR
                sh 'scp target/tu_proyecto.jar usuario@servidor:/ruta/del/proyecto'
            }
        }
    }
}
