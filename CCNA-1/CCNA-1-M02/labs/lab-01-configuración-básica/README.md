# Laboratorio 1 - Configuración básica de Dispositivos

<img width="563" height="346" alt="Captura de pantalla de 2026-03-23 20-02-33" src="https://github.com/user-attachments/assets/a9069873-55de-43dd-94f4-476de82d13a3" />

## Tabla de contenidos

- [Configuración básica del switch](#configuración-básica-del-switch)
  - [Propósito](#propósito)
  - [Topologia de red](#topologia-de-red)
  - [Procedimientos](#procedimientos)
  - [Análisis técnico](#análisis-técnico)

- [Configuración para conectividad básica de dispositivos](#Configuración-para-conectividad-básica-de-dispositivos))
  - [Propósito](#propósito-2)
  - [Topologia de red](#topologia-de-red-2)
  - [Procedimientos](#procedimientos-2)
  - [Análisis técnico](#análisis-técnico-2)

-  [Observaciones finales](#Observaciones-finales)

## Archivos y configuraciones del laboratorio

### Archivos Packet Tracer

- [ARCHIVO 1 - CONFIG. BÁSICA](../../files/basic-config.pka)
- [ARCHIVO 2 - CONECT. BÁSICA](../../files/basic-connectivity.pka)

### Configuraciones basicas de switches

- [SWITCH 1 - CONFIG. BáSICA](../../configs/S1-running-config/)
- [SWITCH 2 - CONFIG. BáSICA](../../configs/S2-running-config/)

### Configuraciones de conectividad

- [SWITCH 1 - CONECT. BÁSICA](./CCNA-1-M02/configs/S1-basic-connectivity)
- [SWITCH 2 - CONECT. BÁSICA](./CCNA-1-M02/configs/S2-basic-connectivity)


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

## Configuración para conectividad básica de dispositivos

<img width="642" height="128" alt="Captura de pantalla de 2026-03-23 20-15-26" src="https://github.com/user-attachments/assets/3b10ab49-8690-468c-871a-32ca1f81a274" />


### Propósito

Realizar configuraciones básicas de conectividad con asignacion de direcciones IP, en switches y PC, verificaciones de correcta implementacion de las configuraciones y conexiones.

### Topologia de Red

2 Switch
2 PCs

### Procedimientos

- **Configuracion basica en los switches**

  - **Análisis**: Se realizan en conjunto los procedimientos básicos de configuración ejemplificados anteriormente, se establece contraseñas de consola y del modo EXEC privilegiado, banner de advertencia de acceso y su correspondiente guardado de archivo mediante el comando `copy running-config startup-config`.


<img width="608" height="292" alt="Captura de pantalla de 2026-03-23 16-22-04" src="https://github.com/user-attachments/assets/05b99a1f-4bb1-47a2-8a28-4011eb59723f" />


<img width="605" height="342" alt="Captura de pantalla de 2026-03-23 16-25-12" src="https://github.com/user-attachments/assets/df4a96f6-f169-40cb-a238-9cbbecc2b447" />

- **Configuracion basica de direcciones IP en PCs**

  - **Análisis**: Se implementan las configuraciones correspondientes para la conectividad de dispositivos dentro de la red, configuracion de direcciones IP y máscara de subred en cada computadora. Y como ejercicio comprobar si con la configuracion únicamente de PCs es posible realizar `ping` a los dispositivos switch. Esto no resulto posible debido a que se deben cumplir ciertos puntos para que sea exitoso el comando. Se debe configurar la interfaz del Switch (En el caso del laboratorio, la interfaz VLAN 1) y se debe encender la interfaz mediante el comando `no shutdown`.

**PC 1**
<img width="1366" height="768" alt="Captura de pantalla de 2026-03-23 16-27-35" src="https://github.com/user-attachments/assets/20d5d4b5-1766-421f-91ef-13493e747727" />

**PC 2**
<img width="1366" height="768" alt="Captura de pantalla de 2026-03-23 16-27-20" src="https://github.com/user-attachments/assets/94b1134a-144d-4d6a-9d12-79959f2a1dac" />


- **Configuracion de interfaces en switches**

  - **Análisis**: Se ejecutan las configuraciones pertinentes para lograr una conectividad completa dentro de la red, se asignan las direcciones IP a cada interfaz de cada switch, encendido de interfaces para lograr que esten visibles y verificacion de la correcta implementacion utilizando el comando `show ip interface brief`.

<img width="604" height="435" alt="Captura de pantalla de 2026-03-23 16-34-38" src="https://github.com/user-attachments/assets/6987b1ad-ced0-4123-8161-b132ee419ef8" />

<img width="610" height="415" alt="Captura de pantalla de 2026-03-23 16-35-15" src="https://github.com/user-attachments/assets/755371c7-b4e4-4791-a5d8-1f6ef0049dfe" />

- **Verificaciones de configuracion y conectividad de la red**

<img width="437" height="408" alt="Captura de pantalla de 2026-03-23 16-37-23" src="https://github.com/user-attachments/assets/d9420ba7-9d1c-4bd6-ab99-eb97a63fb154" />

<img width="572" height="302" alt="Captura de pantalla de 2026-03-23 16-38-52" src="https://github.com/user-attachments/assets/c4158d88-31b2-4f77-b392-016dcf55eebf" />

### Análisis técnico 

Una vez finalizadas las asignaciones de Direcciones IP y mascaras subred descriptas en el cuadro inicial de las PCs y Switches. Se realizan las verificaciones desde cada dispositivo dentro de la red mediante el comando `ping`, se adjuntan verificaciones de ping desde la PC1 y desde el S1 hacia los demas dispositivos dentro la red.

## Estado del sistema

### Inicial

- Dispositivos sin configuración
- Interfaces deshabilitadas
- Sin conectividad

### Final

- Configuración aplicada correctamente
- Interfaces activas
- Red funcional

## Observaciones finales

Mediante el siguiente laboratorio adquiri conocimientos basicos pero primordiales para comenzar a comprender el funcionamiento de una red básica, se logró implementar eficientemente comandos básicos para la puesta a punto de un dispositivo hasta configuraciones de conectividad entre los dispositivos y su consiguiente verificacion. 

Dentro de las observaciones además se notó:
- `enable secret` ofrece mayor seguridad que `enable password` para la securización del modo EXEC privilegiado.
- Se debe aplicar el comando `login` luego de establecer la clave de acceso a la CLI para activarla.
- `no shutdown` es el comando que activa las interfaces de los dispositivos de red
- El primer comando `ping` en primeras instancias puede dar un 80% de resultado aunque todas las direcciones esten configuradas correctamente, esto debido al proceso de ARP y busqueda de dispositivos en la red.
- Comandos de verificacion: `show ip interface brief` `show running-config` `ping`  

[Volver al MÓDULO 2](../)
