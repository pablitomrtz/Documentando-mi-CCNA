# Laboratorio 1 - Configuración básica de Dispositivos

## Propósito

Implementar configuraciones básicas en switches, asegurar el acceso a la interfaz de la CLI y puertos de consola utilizando contraseñas cifradas. Configuración de mensajes para usuarios que inicien sesion en el switch o para advertir usuarios no autorizados.

## Topologia de Red

2 Switch
2 PCs

## Configuraciones

### Configuración básica del switch

- Chequeo de informacion predeterminada del switch 

enable                                     
show running-config                                

- Asignacion de nombre al dispositivo switch

enable 
configure terminal                                   
hostname S1                                          

<img width="422" height="114" alt="Captura de pantalla de 2026-03-23 00-15-21" src="https://github.com/user-attachments/assets/19d45392-9b7d-473f-8661-87c10ebc6fec" />

- Aseguramiento de la linea de consola desde el modo configuracion global

configure terminal
line console 0                                                                            
password letmein
login

<img width="424" height="159" alt="Captura de pantalla de 2026-03-23 00-16-12" src="https://github.com/user-attachments/assets/2efd5e81-4621-4d6a-811f-bcb8bf6f6ddf" />

- Configuración de acceso seguro al modo EXEC privilegiado

enable
configure terminal
enable password c1$c0

<img width="418" height="129" alt="Captura de pantalla de 2026-03-23 00-30-39" src="https://github.com/user-attachments/assets/5920a9d2-be01-4b25-a2ae-f78bfce88350" />

- Configuración de una contraseña encriptada para el acceso seguro al modo EXEC privilegiado

configure terminal
enable secret itsasecret

<img width="459" height="101" alt="Captura de pantalla de 2026-03-23 00-32-47" src="https://github.com/user-attachments/assets/f4be1018-6f4f-46d1-812f-0a5fcb47f6d6" />

- Cifrado de contraseñas enable y console

configure terminal 
service password-encryption

<img width="440" height="117" alt="Captura de pantalla de 2026-03-23 00-35-29" src="https://github.com/user-attachments/assets/c7e9cffb-71bc-4a47-b331-39facfdd9427" />

- Creación de un banner MOTD

configure terminal
banner motd "This is a secure system. Authorized Access Only!"

<img width="520" height="103" alt="Captura de pantalla de 2026-03-23 00-38-26" src="https://github.com/user-attachments/assets/5eb3b2b5-a471-4e28-ba58-995a7637f8b1" />

- Guardado y verificacion de las configuraciones establecidas en la memoria RAM no volatil del switch

copy running-config startup-config

<img width="277" height="91" alt="Captura de pantalla de 2026-03-23 00-42-18" src="https://github.com/user-attachments/assets/09d0f83f-b179-4688-82e5-1257944dd361" />

### Configuracion de interfaces del switch
