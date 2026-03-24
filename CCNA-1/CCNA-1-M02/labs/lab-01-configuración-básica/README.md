# Laboratorio 1 - Configuración básica de Dispositivos

<img width="563" height="346" alt="Captura de pantalla de 2026-03-23 20-02-33" src="https://github.com/user-attachments/assets/a9069873-55de-43dd-94f4-476de82d13a3" />

## Tabla de contenidos

- [Configuración básica del switch](#configuración-básica-del-switch)
  - [Propósito](#propósito)
  - [Topologia de red](#topologia-de-red)
  - [Procedimientos](#procedimientos)
  - [Análisis técnico](#análisis-técnico)

-  [Observaciones finales](#Observaciones-finales)

## Archivos y configuraciones del laboratorio

### Archivos Packet Tracer

- [ARCHIVO 1 - CONFIG. BÁSICA](../../files/basic-config.pka)

### Configuraciones basicas de switches

- [SWITCH 1 - CONFIG. BáSICA](../../configs/S1-running-config/)
- [SWITCH 2 - CONFIG. BáSICA](../../configs/S2-running-config/)

## Configuración básica del switch


### Propósito

Implementar configuraciones básicas en switches, asegurar el acceso a la interfaz de la CLI y puertos de consola utilizando contraseñas cifradas. Configuración de mensajes para usuarios que inicien sesion en el switch o para advertir usuarios no autorizados.

### Topologia de Red

- 2 Switch
- 2 PCs

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

  - **Análisis**: Importante implementar el cifrado en aquellas contraseñas que se almacenan en texto plano dentro del archivo de configuracion de los dispositivos
  
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

### Análisis técnico 

Se logró implementar correctamente una configuración básica completa en los dispositivos de red, incluyendo identificación, securización, buenas practicas como cifrado de contraseñas y configuración de banners de aviso antes de acceder a la linea de comando.

## Estado del sistema

### Inicial

- Dispositivos sin identificación
- Accesos sin configuración
- Falta de encriptación

### Final

- Identificación implementada correctamente
- Claves de acceso en CLI y modo EXEC Privilegiado
- Encriptación 

## Observaciones finales

Mediante el siguiente laboratorio adquiri conocimientos basicos pero primordiales para comenzar a comprender el funcionamiento de una red básica, se logró implementar eficientemente comandos básicos para la puesta a punto de los dispositivos de red. 

Dentro de las observaciones además se notó:
- `enable secret` ofrece mayor seguridad que `enable password` para la securización del modo EXEC privilegiado.
- Se debe aplicar el comando `login` luego de establecer la clave de acceso a la CLI para activarla.

[Volver al MÓDULO 2](../)
