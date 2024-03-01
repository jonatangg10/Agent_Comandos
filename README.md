<p align="center">¡ Bienvenido !</p>
<p align="center"><b>Ejemplo practico de Jenkins</b></p>
<p align="center"><a>Configuración de un <b>Agent</b> y la ejecución de comandos <b>Linux</b></a></p>
<p align="center"><b>Si se puede inmaginar, se puede programar</b></p>

provider "aws" {
  region = "us-west-2"
}

resource "aws_ses_email_identity" "sender" {
  email = "your-email@example.com"
}

resource "null_resource" "send_notification" {
  # Ejecuta el comando para enviar el correo electrónico después de un apply exitoso
  provisioner "local-exec" {
    command = <<-EOT
      aws ses send-email \
        --from sender@example.com \
        --to recipient@example.com \
        --subject "Terraform Apply Success" \
        --text "El proceso de Terraform Apply se ha completado con éxito."
    EOT
  }

  # Solo se ejecuta si el apply tiene éxito
  depends_on = [terraform_apply.success]
}
