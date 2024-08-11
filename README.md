# HC05-Configuraci-n
Código para enviar comandos AT y modificar los parámetros del modulo HC05.

-------------------------------------Ingresar al modo de configuración-------------------------------------------------------

1. Para ingresar en modo de configuración es necesario desconectar el pin vcc del arduino, presionar el botón y conectar nuevamente. Recordar que se debe mantener el botón presionado mientras se conecta la alimentación (vcc), soltar el botón antes de 5 segundos de realizar la conexión, el led debe empezar a parpadear lentamente. (si continua parpadeando con mayor frecuencia volver a repetir el procedimiento).
2. Cargar el código.
3. Enviar comandos AT

------------------------------------------------- Comandos AT ----------------------------------------------------------------

AT                   -->Devuelve "ok" cuando existe comunicación.
AT+ORGL              -->Restaura los valores de fabrica.(Después de enviar este comando se debe volver a ingresar en modo de configuración)
AT+NAME              -->Devuelve el nombre del modulo.
AT+NAME=JG           -->Asigna el nuevo nombre que será JG. 
AT+PSWD              -->Devuelve la contraseña de conexión para el modulo.
AT+PSWD=1234         -->Asigna la nueva contraseña del modulo.
AT+ROLE              -->Devuelve el role del modulo ( 0=Slave, 1=Master). 
AT+ROLE=0            -->Asigna el role del modulo como esclavo.
AT+AURT?             -->Devuelve velocidad de comunicación.
AT+AURT=38400,0,0    -->Asigna velocidad de 38400 baudios (no olvidar digitar ,0,0 para asignar el valor)
AT+RESET             -->Sale del modo de configuración para ser vinculado por un dispositivo externo. (Paso final para implementar el modulo, cuando se envia este comando el led debe empezar a parpadear con mayor frecuencia y no se pueden enviar mas comandos AT)
