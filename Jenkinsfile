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
    post {
        always {
             script {
                    def color = "rojo"
                    echo "${color}"
             }
            emailext subject: "Jenkins: ${currentBuild.getFullDisplayName()}",          
                        body : """
                                <!DOCTYPE html>
                                    <html lang="en">
                                        <head>
                                            <meta charset="UTF-8">
                                            <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                            <title>Notificacion de Jenkins</title>
                                        <style>
                                            body {
                                                font-family: 'Arial', sans-serif;
                                                margin: 0;
                                                padding: 0;
                                                background-color: #f8f9fa;
                                                color: #333333;
                                            }
                                            .container {
                                                max-width: 600px;
                                                margin: 0 auto;
                                                background-color: #fafbfd;
                                                border-radius: 8px;
                                                overflow: hidden;
                                                box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
                                            }
                                            .header {
                                                background-color: #007bff;
                                                padding: 20px;
                                                color: #ffffff;
                                                text-align: center;
                                                font-family: 'Roboto', sans-serif;
                                            }
                                            .content {
                                                padding: 30px;
                                            }
                                            h1 {
                                                font-family: 'Montserrat', sans-serif;
                                                color: white;
                                                font-size: 28px;
                                                margin-top: 0;
                                            }
                                            h2 {
                                                font-family: 'Montserrat', sans-serif;
                                                color: #007bff;
                                                font-size: 24px;
                                            }
                                            p {
                                                font-size: 16px;
                                                line-height: 1.6;
                                            }
                                            a {
                                                color: #007bff;
                                                text-decoration: none;
                                                font-weight: bold;
                                            }
                                            .button {
                                                display: inline-block;
                                                background-color: #007bff;
                                                color: white;
                                                padding: 10px 20px;
                                                text-decoration: none;
                                                border-radius: 4px;
                                                font-family: 'Roboto', sans-serif;
                                                transition: background-color 0.3s ease;
                                            }
                                            .button:hover {
                                                background-color: #0056b3;
                                            }
                                            .footer {
                                                background-color: #fafbfd;
                                                padding: 20px;
                                                text-align: center;
                                                font-size: 14px;
                                                border-radius: 0 0 8px 8px;
                                                border-top: 1px solid #dddddd;
                                                margin-top: 10px;
                                            }
                                            @media screen and (max-width: 600px) {
                                                .container {
                                                    border-radius: 0;
                                                }
                                            }
                                        </style>
                                        </head>
                                        <body>
                                            <br>
                                                <div class="container">
                                                    <div class="header">
                                                        <h1>Notificacion de Jenkins</h1>
                                                    </div>
                                                    <div class="content">
                                                        <p>Estimado usuario,</p>
                                                        <p>Este es un correo electronico de notificacion generado por Jenkins.</p>

                                                        <div style="text-align: center;">
                                                            <h2>Detalles del Build:</h2>
                                                            <p>Numero del Build: <strong>${currentBuild.getFullDisplayName()}</strong></p>
                                                            <p>Estado del Build: <strong>${currentBuild.result}</strong></p>
                                                        </div>
                                                        <div style="text-align: center;">
                                                            <p>Puedes encontrar mas detalles en el siguiente enlace:</p>
                                                            <a href="${BUILD_URL}" class="button" style='color: #FFFFFF'>Ver Build</a>
                                                        </div>
                                                        <div style="text-align: center;">
                                                            <p>Puedes encontrar el repositorio en el siguiente enlace:</p>
                                                            <a href="${env.repoLink}" class="button" style='color: #FFFFFF'>Ver repositorio</a>
                                                        </div>
                                                        <p>Gracias,</p>
                                                        <p>El equipo de Jenkins</p>
                                                    </div>
                                                    <div class="footer">
                                                        <p>Si necesitas ayuda, por favor contactanos a traves de:</p>
                                                        <p>Telefono: +57 314 297 5647</p>
                                                        <p>Correo electronico: jonatangutierrez@seti.com.co</p>
                                                        <p>Visita nuestra pagina web: <a href="https://www.ejemplo.com">www.ejemplo.com</a></p>
                                                    </div>
                                                </div>
                                        </body>
                                </html>
                                """,
                        to: "marianalaverde29@gmail.com",
                        // to: "jonatangutierrez@seti.com.co",
                        //from: "mariaeugenianieto345@gmail.com",
                        from: "jonatangutierrez@seti.com.co",
                        replyTo: "jonatangutierrez@seti.com.co",
                        //charsetStr: "UTF-8",
                        //charset: "UTF-8",
                        mimeType: 'text/html'
        }
    }
    
}
