# Laboratorio 3 - Configuración de una Red Simple

<img width="543" height="288" alt="Captura de pantalla de 2026-03-24 16-38-58" src="https://github.com/user-attachments/assets/f026982a-9e45-4d6a-92e1-8d10cb57e5b4" />

## Tabla de contenido

- [Configuración de una red simple](#Configuración-de-una-red-simple)
  - [Propósito](#propósito)
  - [Topologia de red](#topologia-de-red)
  - [Procedimientos](#procedimientos)
  - [Análisis técnico](#análisis-técnico)
  
## Archivos y configuraciones

### Archivo Packet Tracer

- [ARCHIVO - RED SIMPLE](../../files/red-pequeña.pka)

### Configuraciones de Switches

- [SWITCH 1 - RED SIMPLE](../..//configs/S1-red-pequeña)
- [SWITCH 2 - RED SIMPLE](../../configs/S2-red-pequeña)


## Configuración de una red simple

### Propósito 

Configuración de una red LAN pequeña. Configuración básica de los dispositivos de la red y configuración de parámetros de conexión como direcciones IP a los dispositivos host y switches para proporcionar una conectividad completa en la red.  

### Topologia de red

- 2 PCs
- 2 Switch

### Procedimientos

- **Acceso a la CLI del Switch mediante conexión de consola**

<img width="1366" height="768" alt="Captura de pantalla de 2026-03-24 16-48-39" src="https://github.com/user-attachments/assets/7c377afe-760b-45b1-b72b-2f4e66eb7164" />

- **Configuración básica de identificacion, implementación de contraseñas, y encriptación**
  - **Análisis**: Se implementan las configuraciones básicas de puesta a punto de un switch, como identificación, claves de acceso en todas las lineas y en el modo EXEC privilegiado, su correspondiente aviso y cifrado completo de contraseñas. esta vez se realizó el proceso desde una conexión por consola, simulando un acceso a la CLI por computadora.

<img width="487" height="255" alt="Captura de pantalla de 2026-03-24 17-05-15" src="https://github.com/user-attachments/assets/3f075f36-a597-4549-b4e8-670cd18ecba8" />

- **Configuración de conectividad de dispositivos**
  - **Análisis**: Se lleva a cabo la onfiguración de procedimientos para el direccionamiento IP de todos los dispositivos de acuerdo con la tabla de direccionamiento.

<img width="652" height="127" alt="Captura de pantalla de 2026-03-24 17-14-42" src="https://github.com/user-attachments/assets/7e145a94-9711-4bba-9370-c81dd7e23db1" />

**PC Manager**

<img width="674" height="336" alt="Captura de pantalla de 2026-03-24 17-09-33" src="https://github.com/user-attachments/assets/1b5b182b-6298-4690-9fe7-ae36d3134eb5" />


**Switch Room-145**

<img width="569" height="168" alt="Captura de pantalla de 2026-03-24 17-08-51" src="https://github.com/user-attachments/assets/a4cb6319-a8c4-4a5e-bd2c-3a77656d3b80" />

- **Verificacion de conectividad**
  - **Análisis**: Mediante el comando ping se realizan las verificaciones de conectividad y funcionamiento correcto de la red. En las imagenes se realiza ping desde la PC Reception y desde el switch Room-145

**PC Reception**

<img width="431" height="546" alt="Captura de pantalla de 2026-03-24 17-26-53" src="https://github.com/user-attachments/assets/ba6d6988-9b39-40d7-8227-62390784d025" />


**Switch Room-145**

<img width="530" height="301" alt="Captura de pantalla de 2026-03-24 17-29-53" src="https://github.com/user-attachments/assets/25f15464-d717-40d7-96a5-80a74268fb18" />


### Análisis técnico

Se implemento exitosamente las configuraciones basicas para el funcionamiento de una red simple, trabajo que simula un caso real de un técnico de LAN y los pasos que deberia seguir para lograr poner en marcha una red simple, entre ellos configuraciones de nombrado, contraseñas, direccionamiento y posterior verificación. En el transcurso del desarrollo del trabajo atravese un problema donde se paso por alto la configuracion de claves de acceso en todas las lineas, olvidandose de configurar una clave para las lineas VTY, error que fue corregido posteriormente luego de leer las instrucciones correctamente. 

[Volver al MÓDULO 2](../)
