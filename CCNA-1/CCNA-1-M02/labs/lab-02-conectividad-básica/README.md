# Laboratorio 2 - Configuraciones de conectividad de Dispositivos

<img width="563" height="346" alt="Captura de pantalla de 2026-03-23 20-02-33" src="https://github.com/user-attachments/assets/a9069873-55de-43dd-94f4-476de82d13a3" />

## Tabla de contenidos

- [Configuración para conectividad básica de dispositivos](#Configuración-para-conectividad-básica-de-dispositivos))
  - [Propósito](#propósito-1)
  - [Topologia de red](#topologia-de-red-1)
  - [Procedimientos](#procedimientos-1)
  - [Análisis técnico](#análisis-técnico-1)

-  [Observaciones finales](#Observaciones-finales)

## Archivos y configuraciones del laboratorio

### Archivos Packet Tracer

- [ARCHIVO - CONECT. BÁSICA](../../files/basic-connectivity.pka)

### Configuraciones de conectividad

- [SWITCH 1 - CONECT. BÁSICA](../../configs/S1-basic-connectivity)
- [SWITCH 2 - CONECT. BÁSICA](../../configs/S2-basic-connectivity)

## Configuración para conectividad básica de dispositivos

<img width="642" height="128" alt="Captura de pantalla de 2026-03-23 20-15-26" src="https://github.com/user-attachments/assets/3b10ab49-8690-468c-871a-32ca1f81a274" />


### Propósito

Realizar configuraciones básicas de conectividad con asignacion de direcciones IP, en switches y PC, verificaciones de correcta implementacion de las configuraciones y conexiones.

### Topologia de Red

- 2 Switch
- 2 PCs

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
