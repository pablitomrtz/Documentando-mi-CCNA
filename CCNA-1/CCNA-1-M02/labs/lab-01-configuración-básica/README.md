# Laboratorio 1 - Configuración básica de Dispositivos


## Configuración básica del switch


### Propósito

Implementar configuraciones básicas en switches, asegurar el acceso a la interfaz de la CLI y puertos de consola utilizando contraseñas cifradas. Configuración de mensajes para usuarios que inicien sesion en el switch o para advertir usuarios no autorizados.

### Topologia de Red

2 Switch
2 PCs

### Procedimientos

- **Chequeo de informacion predeterminada del switch** 

```
enable                                     
show running-config                                
```


- **Asignacion de nombre al dispositivo switch**

```
enable 
configure terminal                                   
hostname S1                                          
```

<img width="422" height="114" alt="Captura de pantalla de 2026-03-23 00-15-21" src="https://github.com/user-attachments/assets/19d45392-9b7d-473f-8661-87c10ebc6fec" />


- **Aseguramiento de la linea de consola desde el modo configuracion global**

  - **Análisis**: Se asigna acceso seguro a la linea de consola con contraseña, tener en cuenta ingresar el comando login ya que es indispensable para indicar al sistema que antes de dar acceso al CLI debe ingresar mediante una clave. En el caso del ejemplo, letmein

```
configure terminal
line console 0                                                                            
password letmein
login
```

<img width="424" height="159" alt="Captura de pantalla de 2026-03-23 00-16-12" src="https://github.com/user-attachments/assets/2efd5e81-4621-4d6a-811f-bcb8bf6f6ddf" />


- **Configuración de acceso seguro al modo EXEC privilegiado**

  - **Análisis**: Se establece la contraseña al modo EXEC privilegiado, hasta ahora, estas contraseñas no estan aseguradas, si accedemos al archivo de configuraciones del switch podemos dictaminar que estas son guardadas en texto plano, lo que seria una vulnerabilidad altamente critica para una red.

```
enable
configure terminal
enable password c1$c0
```

<img width="418" height="129" alt="Captura de pantalla de 2026-03-23 00-30-39" src="https://github.com/user-attachments/assets/5920a9d2-be01-4b25-a2ae-f78bfce88350" />


- **Configuración de una contraseña encriptada para el acceso seguro al modo EXEC privilegiado**

  - **Análisis**: Como buena practica es de mayor utilidad utilizar el comando `enable secret` para establecer la clave de acceso al modo EXEC privilegiado, ya que esta se guarda encriptada dentro del contenido del archivo de configuracion del switch.

```
configure terminal
enable secret itsasecret
```

<img width="459" height="101" alt="Captura de pantalla de 2026-03-23 00-32-47" src="https://github.com/user-attachments/assets/f4be1018-6f4f-46d1-812f-0a5fcb47f6d6" />


- **Cifrado de contraseñas enable y console**

```
configure terminal 
service password-encryption
```

<img width="440" height="117" alt="Captura de pantalla de 2026-03-23 00-35-29" src="https://github.com/user-attachments/assets/c7e9cffb-71bc-4a47-b331-39facfdd9427" />


- **Creación de un banner MOTD**

```
configure terminal
banner motd "This is a secure system. Authorized Access Only!"
```

<img width="520" height="103" alt="Captura de pantalla de 2026-03-23 00-38-26" src="https://github.com/user-attachments/assets/5eb3b2b5-a471-4e28-ba58-995a7637f8b1" />


- **Guardado y verificacion de las configuraciones establecidas en la memoria RAM no volatil del switch**

```
copy running-config startup-config
```

<img width="277" height="91" alt="Captura de pantalla de 2026-03-23 00-42-18" src="https://github.com/user-attachments/assets/09d0f83f-b179-4688-82e5-1257944dd361" />


### Configuracion de interfaces del switch

### Propósito

Realizar configuraciones básicas de conectividad con asignacion de direcciones IP, en switches y PC, verificaciones de correcta implementacion de las configuraciones y conexiones.

### Topologia de Red

2 Switch
2 PCs

- Configuracion basica en los switches

<img width="608" height="292" alt="Captura de pantalla de 2026-03-23 16-22-04" src="https://github.com/user-attachments/assets/05b99a1f-4bb1-47a2-8a28-4011eb59723f" />

<img width="605" height="342" alt="Captura de pantalla de 2026-03-23 16-25-12" src="https://github.com/user-attachments/assets/df4a96f6-f169-40cb-a238-9cbbecc2b447" />

- Configuracion basica de direcciones IP en PCs

PC 1
<img width="1366" height="768" alt="Captura de pantalla de 2026-03-23 16-27-35" src="https://github.com/user-attachments/assets/20d5d4b5-1766-421f-91ef-13493e747727" />

PC 2
<img width="1366" height="768" alt="Captura de pantalla de 2026-03-23 16-27-20" src="https://github.com/user-attachments/assets/94b1134a-144d-4d6a-9d12-79959f2a1dac" />

- Configuracion de interfaces en switches

<img width="604" height="435" alt="Captura de pantalla de 2026-03-23 16-34-38" src="https://github.com/user-attachments/assets/6987b1ad-ced0-4123-8161-b132ee419ef8" />

- Verificaciones de configuracion y conectividad de la red

<img width="610" height="415" alt="Captura de pantalla de 2026-03-23 16-35-15" src="https://github.com/user-attachments/assets/755371c7-b4e4-4791-a5d8-1f6ef0049dfe" />


<img width="437" height="408" alt="Captura de pantalla de 2026-03-23 16-37-23" src="https://github.com/user-attachments/assets/d9420ba7-9d1c-4bd6-ab99-eb97a63fb154" />

<img width="572" height="302" alt="Captura de pantalla de 2026-03-23 16-38-52" src="https://github.com/user-attachments/assets/c4158d88-31b2-4f77-b392-016dcf55eebf" />

