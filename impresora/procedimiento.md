# Procedimiento
0. Prender la impresora.
    * En la zapatilla está conectada, por un lado, la impresora y, por otro lado, una Raspberry Pi, que es la que corre el servidor de [Octoprint](https://octoprint.org) para poder imprimir desde la computadora (Fijarse que la zapatilla esté conectada y prendida).
    > No hace falta descargar nada para usar Octoprint.

    ![boton de encendido](./imagenes/boton.jpg)
    ![zapatilla](./imagenes/zapatilla.jpg)
1. Limpiar la cama.
2. [Nivelar la cama](./nivelación.md).
3. Descargar el archivo STL de la pieza a imprimir.
4. Luego de haber instalado y configurado el slicer de acuerdo con el documento de [instalación](./apps-y-archivos-requeridos.md), seguir los siguientes pasos en la pestaña "Preparar":
    * Agregar el objeto (STL de la/s pieza/s).

    ![Paso 10](imagenes/instalacion-orca-10.png)
    ![Paso 11](imagenes/instalacion-orca-11.png)
    * Realizar el laminado (Slicear).
    ![Paso 12](imagenes/instalacion-orca-12.png)
    * Generar el código G (Gcode).
    ![Paso 13](imagenes/instalacion-orca-13.png)
> Nota: Los pasos siguientes también se pueden hacer de [forma manual](./control-con-lcd.md) sin utilizar la computadora, a través de los comandos de la pantalla LED de la propia impresora.
5. Entrar a [Octoprint en esta URL](https://mecabot.ingenieria) e ingresar utilizando las credenciales.
<p align="center">
  <img src="./imagenes/octoprint-1.png" />
</p>

> Lo anterior es para cuando se está conectado a la red de MECACUEVA o a cualquiera de las redes del DETI I. Para poder controlar la impresora desde otra red usamos [Tailscale](https://tailscale.com/), para eso seguir los pasos indicados [mas abajo](#obtener-url-para-tailscale)

6. Verificar que la impresora esté conectada a la RASPBERRY a través del cable USB para poder controlarla.

![Conexión Raspberry](./imagenes/conexion-raspy.png)

## Obtener URL para Tailscale
* Instalar [Tailscale](https://tailscale.com/download) y crear una [cuenta](https://login.tailscale.com/login)
* Pedir el link de acceso al nodo de la impresora al [Mail de la Asociación](asocdemecauncuyo@gmail.com) o directamente al que corresponda. Poner en el asunto **ACCESO-REMOTO-IMPRESORA**. Enviar desde el mail con el que se registró a la convocatoria de miembros de la Asociación.
* Al recibir la URL de invitación, aceptarla. El nodo va a aparecer en la lista de dispositivos del panel admin de su cuenta de Tailscale.

![tailscale device](./imagenes/tailscale.png)
* Copiar la dirección IP que aparece para el dispositivo.
* Ingresar al panel de Octoprint en ***https://\<IP\>***
* Continuar desde el paso 5.
