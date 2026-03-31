# Módulo 3 - Protocolos y modelos de red

## Laboratorios

- [Laboratorio 1 - Investigación del Modelo OSI](./labs/lab-01-modelos/)
- [Laboratorio 2]
- [Laboratorio 3]

## Protocolos

Conjunto de reglas que definen un formato de reglas para el intercambio de datos e informacion por la red. Cada protocolo tiene su propósito, formato y regla para la comunicación. Entre sus funciones encontramos:

- Direccionamiento
- Confiabilidad
- Control de flujo
- Secuenciación
- Detección de errores

### Tipos de protocolo

| Tipo de Protocolo | Descripción | Ejemplos |
|------|---------|-------------|
|**Protocolos de comunicaciones de red** | Permiten que dos o mas dispositivos se comuniquen a traves de ellos | `IP` `TCP` `HTTP` |
| **Protocolos de seguridad de red** | Proporcionan protección a los datos a traves de mecanismos de autenticación, cifrado e integridad de datos | `SSH` `SSL` `TLS` |
| **Protocolos de routing** | Otorgan a los routers la capacidad de tomar decisiones sobre que ruta utilizaran para enviar los datos al destino a traves de la mejor ruta | `OSPF` `BGP` |
| **Protocolos de detección de servicios** | Utilizado para detección automática de dispositivos o servicios | `DHCP` `DNS` |

## Suites de protocolos

<img width="444" height="260" alt="Captura de pantalla de 2026-03-30 19-39-40" src="https://github.com/user-attachments/assets/4a8fa760-9f12-4e87-96d4-9291ad86e65e" />

Es un conjunto de protocolos que trabajan conjuntamente para proporcionar servicios integrales de comunicación de red. 
Ejemplos: TCP/IP - Modelo OSI - AppleTalk - Novell NetWare

### Suite de protocolos TCP/IP

Es el conjunto de protocolos utilizado hoy en dia por internet y las redes. Destaca en dos aspectos, es una suite de protocolos de estandar abierto, siendo disponible para todo publico y utilizable por cualquier proveedor en su hardware o software, y tambien, que es una suite de protocolos basada en estandares, es decir que es respaldada y aprobada por organizaciones de estandares, asegurando interoperatividad entre distintos productos fabricantes.

### Capas de protocolo TCP/IP 

**Capa de aplicación**
  
- Sistema de nombres:
  - `DNS` - Domain Name System, traduce dominios a direcciones IP.
  - `DHCPv4` - Protocolo de configuración dinamica de host para IPv4.
  - `DHCPv6` - Protocolo de configuración dinamica de host para IPv6.

- Correo electrónico
  - `SMTP` - Protocolo de Transferencia Simple de Correo. Permite a clientes enviar correos electrónicos a un servidor de correo y a su vez permite servidores enviar correos a otros servidores.
  - `POP3` - Protocolo de Oficina de Correo v3. Permite la recuperacion de correos de un servidor y descargarlo en la app de correo del cliente.
  - `IMAP` - Protocolo de Acceso a Mensajes de Internet. Permite el acceso a clientes a correos almacenados en los servidores de correo electrónico.

- Transferencia de Archivos
  - `FTP` - Protocolo de Transferencia de Archivos. Establece reglas que permiten a un host acceder y transferir archivos hacia o desde otro host por la red.
  - `SFTP` - SSH Protocolo de Transferencia de Archivos. Establece una conexión segura mediante el protocolo SSH para el inicio remoto seguro para acceder a la CLI del host
  - `TFTP` - Protocolo de Transferencia de Archivo Trivial. Transferencia de archivos simple y sin conexión con la entrega de archivos sin reconocimiento.

- Web y Servicio Web
  - `HTTP` - Protocolo de Transferencia de Hipertexto. Protocolo para el intercambio de texto, imagenes, sonido, videos y demas archivos en la WWW.
  - `HTTPS` - Protocolo HTTP seguro. Cifra los datos que se transfireren por la WWW.

**Capa de transporte**

- Orientado a conexión
  - `TCP` - Protocolo de Control de Transmisión. Permite comunicación confiable entre procesos en hosts independientes, cuenta con transmision fiable y con acuse de recibo.
  - `UDP` - Protocolo de Datagramas de Usuario. No confirma transmisión correcta de datagramas, habilita un proceso que se ejecuta en un host para enviar paquetes a un proceso ejecutado en otro host.

**Capa de Internet**

- Protocolo de Internet
  - `IPv4` - Protocolo de Internet v4. Recibe segmentos de mensaje de la capa de transporte, empaqueta mensajes en paquetes y dirige paquetes hasta su destino. Utiliza direcciones de 32 bits.
  - `IPv6` - IP version 6. Utiliza direcciones de 128 bits.
  - `NAT` - Traducción de Direcciones de Red. Traduce direcciones IPv4 de una red privada en direcciones IPv4 públicas únicas.

**Capa de Acceso de Red**

- Resolución de dirección
  - `ARP` - Protocolo de Resolución de Direcciones. Proporciona la asignación de direcciones dinámicas entre una direccion IP y una direccion MAC.

- Protocolos de Enlace de Datos
  - `Ethernet` Define reglas para conectar y señalizar estándares de la capa de acceso a red.
  - `WLAN` - Wireless Local Area Network. Define reglas para señalización inalámbrica por medio de frecuencias de radio de 2.4 GHz y 5 GHz.

### Proceso de comunicación TCP/IP

La encapsulación describe cómo los datos se transforman al viajar por la red.
Flujo:  Datos → Segmentos → Paquetes → Tramas → Bits
Cada capa agrega información necesaria para que el mensaje llegue correctamente a destino.

### Modelo de Referencia OSI

Proporciona una lista de servicios que estan presentes en cada capa, es coherente con todos los tipos de servicios y protocolos de red, describiendo que se debe hacer en una capa determinada pero sin regir la manera en que se debe lograr. Describe la interaccion de cada capa con la capa por encima y por debajo. 

**Capas del modelo OSI**
- Aplicación
- Presentación
- Sesión
- Transporte
- Red
- Enlace de Datos
- Fisica

### Modelo de protocolo TCP/IP

Modelo para comunicaciones de internet, coincide con la  estructura de una suite de protocolos determinada. Describe las funciones que ocurren en cada capa de protocolos dentro de una suite de TCP/IP.

**Capas de modelo TCP/IP**
- Aplicación
- Transporte
- Internet
- Acceso a la red

### Comparación de Modelo OSI y Modelo TCP/IP

<img width="572" height="372" alt="Captura de pantalla de 2026-03-30 20-30-13" src="https://github.com/user-attachments/assets/f544d976-e2dc-4224-b138-cd95f0d7b231" />

- La capa 3 de red en el Modelo OSI, esta asignada a la capa de Internet TCP/IP.
- La capa 4 de transporte OSI, esta asignada directamente a la capa de transporte en el modelo TCP/IP.
- La capa de aplicación de TCP/IP incluye los protocolos 5, 6 y 7 del modelo OSI.

