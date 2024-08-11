# HC05-Configuraci-n
Código para enviar comandos AT y modificar los parámetros del modulo HC05.

------------------------------- Comandos AT ------------------------------------

AT                   -->Devuelve "ok" cuando existe comunicación.
AT+ORGL              -->Restaura los valores de fabrica.
AT+NAME              -->Devuelve el nombre del modulo.
AT+NAME=JG           -->Asigna el nuevo nombre que será JG. 
AT+PSWD              -->Devuelve la contraseña de conexión para el modulo.
AT+PSWD=1234         -->Asigna la nueva contraseña del modulo.
AT+ROLE              -->Devuelve el role del modulo ( 0=Slave, 1=Master). 
AT+ROLE=0            -->Asigna el role del modulo como esclavo.
AT+AURT?             -->Devuelve velocidad de comunicación.
AT+AURT=38400,0,0    -->Asigna velocidad de 38400 baudios (no olvidar digitar ,0,0 para asignar el valor)
AT+RESET             -->Sale del modo de configuración para ser vinculado por un dispositivo externo.

