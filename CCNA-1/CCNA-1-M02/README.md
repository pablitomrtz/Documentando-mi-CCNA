# Módulo 2

Este módulo dicta configuraciones básicas e iniciales de dispositivos en una red utilizando la CLI de Cisco IOS, comandos básicos y pruebas de funcionalidad. Dentro de este writeup incluí teoría básica abarcando desde el SO encargado del funcionamiento de los dispositivos hasta comandos básicos para una correcta implementación de configuraciones en una red. Al completar este módulo, comprenderás cómo configurar dispositivos de red desde cero y verificar su correcto funcionamiento.

## Laboratorios

- [Laboratorio 1 - Configuración Básica de Dispositivos](./labs/lab-01-configuración-básica/)
- [Laboratorio 2 - Configuración Básica de Conectividad](./labs/lab-02-conectividad-básica/)
- [Laboratorio 3 - Configuración de una red simple](./labs/lab-03-red-simple/)
## Tabla de Contenidos

- [Sistemas Operativos](#sistemas-operativos)
- [Cisco IOS](#cisco-ios)
  - [Estructura de Comandos](#estructura-de-comandos)
  - [Modos de Comando](#modos-de-comando)
  - [Comandos de Navegación](#comandos-de-navegación)
  - [Comandos de Verificación](#comandos-de-verificación)
  - [Teclas de Acceso Rápido](#teclas-de-acceso-rápido)

## Sistemas Operativos

Es el software principal dentro de un dispositivo, se encarga de la gestión eficiente del hardware (Memoria RAM, Discos Duros, Procesador, etc.) para proporcionar servicios a través de una interfaz de usuario a los programas de aplicación.

- **Shell**: interfaz que puede tratarse de una CLI (PowerShell, bash, cmd.exe, etc.) o una GUI (GNOME, Escritorio de Windows), encargada de la interacción con las aplicaciones y el usuario.
- **Kernel**: encargado de la comunicación entre hardware y software de la computadora, administra los recursos de hardware.

## Cisco IOS

Es el sistema operativo utilizado en dispositivos de red como routers y switches. Permite administrar, configurar y monitorear el funcionamiento de la red mediante una CLI. A través de IOS, un administrador puede hacer lo siguiente:

- Configurar dispositivos
- Gestionar interfaces
- Verificar el estado de la red
- Aplicar políticas básicas

### Estructura de Comandos

![Estructura de comandos Cisco IOS](https://github.com/user-attachments/assets/5e55be7f-2cef-4dce-afc2-5e6f5fe5dcaf)

| Término | Descripción |
|---------|-------------|
| **Palabra clave** | Parámetro específico definido en el SO (ej: ip protocols) |
| **Argumento** | Valor o variable definida por el usuario o administrador (ej: 192.168.10.5) |

### Modos de Comando

| Modo | Símbolo | Descripción |
|------|---------|-------------|
| EXEC de Usuario | `>` | Capacidades limitadas, ofrece operaciones básicas de monitoreo, no permite cambios en la configuración del dispositivo. |
| EXEC Privilegiado | `#` | Permite ejecutar comandos de configuración y acceso a modos de configuración más avanzados. |
| Configuración Global | `(config)#` | Tipo de configuración avanzada que permite la configuración completa del dispositivo. |

**Ejemplo de modos:**

```
Router>                 # Modo EXEC usuario
Router#                 # Modo EXEC privilegiado
Router(config)#         # Modo de configuración global
```

### Comandos de Navegación

| Comando | Descripción |
|---------|-------------|
| `enable` | Accede al modo EXEC privilegiado desde el modo EXEC usuario. |
| `disable` | Vuelve al modo EXEC usuario desde el modo EXEC privilegiado. |
| `configure terminal` | Ingresa al modo configuración global desde el modo EXEC privilegiado. |
| `exit` | Vuelve al modo anterior (desde config global a EXEC privilegiado). |

**Ejemplo - Acceso a configuración de línea (consola):**

```
Router(config)#line console 0
Router(config-line)#
```

**Ejemplo - Acceso a líneas de administración remota:**

```
Router(config)#line vty 0 4
Router(config-line)#
```

**Ejemplo - Configuración de interfaces:**

```
Router(config)#interface FastEthernet0/1
Router(config-if)#
```

### Comandos de Verificación

Utilizados para validar configuraciones y estado del dispositivo, son comandos fundamentales para comprobar que la configuración aplicada es correcta:

| Comando | Descripción |
|---------|-------------|
| `show running-config` | Muestra la configuración actual de los dispositivos. |
| `show ip interface brief` | Muestra un resumen de línea de las interfaces configuradas. |

### Teclas de Acceso Rápido

| Combinación de Teclas | Función |
|-----------------------|---------|
| `Tab` | Completa la entrada de un comando escrito parcialmente. |
| `Retroceso` o `Ctrl+D` | Borra un carácter a la izquierda del cursor. |
| `Ctrl+U` o `Ctrl+X` | Borra todos los caracteres desde el cursor hasta el comienzo de la línea de comandos. |
| `Ctrl+W` | Borra la palabra a la izquierda del cursor. |
| `Ctrl+A` | Desplaza el cursor al principio de la línea. |
| `Ctrl+E` | Desplaza el cursor al final de la línea. |
| `Esc B` | Desplaza el cursor una palabra a la izquierda. |
| `Esc F` | Desplaza el cursor una palabra a la derecha. |
| `Ctrl+P` | Recupera comandos en el historial. |
| `Ctrl+C` | Finaliza el modo de configuración actual y vuelve al modo EXEC privilegiado. |
| `Ctrl+Shift+6` | Interrupción multipropósito para anular búsquedas DNS, ping, traceroute, etc. |

[Volver a CCNA 1](../)
