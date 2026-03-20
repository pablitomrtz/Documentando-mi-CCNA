# Módulo 2

Este modulo dicta configuraciones basicas e iniciales de dispositivos en una red utilizando la CLI de Cisco IOS, comandos basicos y pruebas de funcionalidad. Dentro de este writeup inclui teoria basica abarcando desde el SO encargado del funcionamiento de los dispositivos hasta comandos basicos para una correcta implementacion de configuraciones en una red.

## Laboratorios

[Laboratorio 1 - Configuración Básica de Dispositivos](./CCNA-1/CCNA-1-M02/ labs/lab-01-configuración-básica/)


## Tabla de contenidos

sistemas operativos
cisco ios

## Sistemas operativos 

Es el software principal dentro de un dispositivo, se encarga de la gestion eficiente del hardware (Memoria RAM, Discos Duros, Procesador, etc.) para proporcionar servicios a traves de una interfaz de usuario a los programas de aplicacion.

- Shell: interfaz que, puede tratarse de una CLI (PowerShell, bash, cmd.exe, etc.) o una GUI (GNOME, Escritorio de Windows), encargada de la interaccion con las aplicaciones y el usuario.
- Kernel: encargado de la comunicacion entre hardware y software de la computadora, administra los recursos de hardware

## Cisco IOS

Es el sistema operativo utilizado en dispositivos de red como routers y switches.
Permite administrar, configurar y monitorear el funcionamiento de la red mediante una CLI. A través de IOS, un administrador puede:
- Configurar dispositivos
- Gestionar interfaces
- Verificar el estado de la red
- Aplicar políticas básicas

### Estructura de comandos

<img width="593" height="249" alt="Captura de pantalla de 2026-03-20 17-20-47" src="https://github.com/user-attachments/assets/5e55be7f-2cef-4dce-afc2-5e6f5fe5dcaf" />

- Palabra clave: es un parametro especifico definido en el SO (ip protocols)
- Argumento: valor o variable definida por el usuario o administrador (192.168.10.5)

### Modos de comando 

- Modo EXEC de usuario (>): capacidades limitadas, ofrece operaciones basicas de monitoreo, no permite cambios en la configuracion del dispositivo.
- Modo EXEC privilegiado (#): permite ejecutar comandos de configurcion y acceso a modos de configuracion mas avanzados.
- Modo de configuracion global (config)#: tipo de configuracion avanzada que permite la configuracion del dispositivo

Ejemplo de modos:

  Router>                # Modo EXEC usuario
  Router#                # Modo EXEC privilegiado
  Router(config)#        # Modo de configuracion global

### Comandos de navegacion

- Comando enable: utilizado para acceder al modo EXEC privilegiado desde el modo EXEC usuario. Comando disable para volver al modo EXEC usuario.
    
    Router>enable
    Router#

- Comando configure terminal: comando para ingresar al modo configuracion global desde el modo EXEC privilegiado. Comando exit para volver al modo EXEC privilegiado

    Router#configure terminal
    Router(config)#

- line: es un tipo de modo de subconfiguracion para acceder a las configuracion de linea, define caracteristicas de acceso a dispositivos ya sea por conexion por consola o por Telnet/SSH.

    Router(config)#line console 0            # Acceso a conexion por consola
    Router(config-line)#

    Router(config)#line vty 0 4              # Acceso a 4 lineas de administracion remota
    Router(config-line)#
  
- interface: modo de subconfiguracion de interfaces

    Router(config)#interface FastEthernet0/1
    Router(config-if)#

### Comandos de verificacion
Utilizados para validar configuraciones y estado del dispositivo, son comandos fundamentales para comprobar que la configuración aplicada es correcta:

- show running-config              # Muestra la configuracion actual de los dispositivos
- show ip interface brief          # Muestra una linea resumida de las interfaces                                             configuradas

### Teclas de acceso rapido

- Tab: completa la entrada de un comando escrito parcialmente
- Retroceso o Ctrl+D: borra un caracter a la izquierda del cursor
- Ctrl+U o Ctrl+X: borra todos los caracteres desde el cursor hasta el comienzo de la linea de comandos
- Ctrl+W: borra la palabra a la izquierda del cursor
- Ctrl+A: desplaza el cursor al principio de la linea
- Ctrl+E: desplaza el cursor al final de la linea
- Esc B: desplaza el cursor una palabra a la izquierda
- Esc F: desplaza el cursor una palabra a la derecha
- Ctrl+P: recupera comandos en el historial
- Ctrl+C: finaliza el modo de configuracion en el que se encuentre y vuelve al modo EXEC privilegiado.
- Ctrl+Shift+6: interrupcion multiproposito para anular busquedas DNS, ping, traceroute, etc.
  


