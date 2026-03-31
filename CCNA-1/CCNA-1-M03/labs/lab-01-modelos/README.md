# Laboratorio 1 - Investigación de Modelos OSI y TCP/IP

<img width="360" height="163" alt="Captura de pantalla de 2026-03-30 20-42-33" src="https://github.com/user-attachments/assets/7ce8a5d8-a185-4014-936b-6f1634e40f9b" />

## Tabla de contenidos

- [Configuración básica del switch](#configuración-básica-del-switch)
  - [Propósito](#propósito)
  - [Topologia de red](#topologia-de-red)
  - [Procedimientos](#procedimientos)
  - [Análisis técnico](#análisis-técnico)

-  [Observaciones finales](#Observaciones-finales)

## Archivos y configuraciones del laboratorio

### Archivos Packet Tracer



### Configuraciones basicas de switches


## Configuración básica del switch


### Propósito

Comprender el conjunto de protocolos TCP/IP y cual es su relacion con el modelo OSI.

### Topologia de Red

- 1 Servidor Web
- 1 PC Cliente Web

### Procedimientos

**Comprension del modo Simulacion y busqueda de trafico HTTP**
  - **Análisis**: Dentro de la aplicación PacketTracer se ingresó al apartado Simulación, en el apartado de lista de evento se seleccionó para que unicamente sean visibles eventos de HTTP.

<img width="684" height="723" alt="Captura de pantalla de 2026-03-30 21-17-44" src="https://github.com/user-attachments/assets/79647246-5c22-4cff-ad78-89ed41515d03" />

**Ingreso desde la PC cliente al servidor web para generar tráfico web**
  - **Análisis**: Se ingresa desde la PC al apartado Web Browser del Escritorio al Servidor web por medio de su dominio www.osi.local. Luego se capturan una cantidad de paquetes dando en Forward para su posterior análisis.

<img width="1366" height="768" alt="Captura de pantalla de 2026-03-30 21-37-27" src="https://github.com/user-attachments/assets/ac07d3e3-3d93-4bb5-b984-b32c006c21ec" />

**Análisis de los paquetes HTTP capturados**
  -**Análisis**: Se ingresa a la PDU HTTP, en el se identifica las capas de entrada y salida, en el paquete seleccionado solamente se ven salidas desde el dispositivo cliente.

<img width="679" height="418" alt="Captura de pantalla de 2026-03-30 21-47-15" src="https://github.com/user-attachments/assets/92978d3f-6dd9-4e53-8831-1d9490021439" />

  - En el apartado Outbound Details, tambien se puede observar en un formato PDU, este paquete permite observar informacion como puertos utilizados, direcciones IP y MAC.

<img width="567" height="550" alt="Captura de pantalla de 2026-03-30 21-49-41" src="https://github.com/user-attachments/assets/110c1f16-97d0-4205-a64d-15cbd0e362df" />

**Análisis completo de paquetes involucrados en la conexión entre dispositivos**
  - **Análisis**: Se analiza completamente las capas y protocolos utilizados en toda la comunicación establecida para que el Cliente pueda acceder a la informacion almacenada dentro del Servidor Web.

<img width="384" height="539" alt="Captura de pantalla de 2026-03-30 21-53-23" src="https://github.com/user-attachments/assets/24155804-63d5-415e-a390-b6e61358cfff" />

<img width="469" height="417" alt="Captura de pantalla de 2026-03-30 21-55-34" src="https://github.com/user-attachments/assets/dbc5cffb-ed21-463f-a4b7-6dc3f4c4efc1" />

<img width="623" height="543" alt="Captura de pantalla de 2026-03-30 21-58-25" src="https://github.com/user-attachments/assets/e639177f-7b1d-421c-8297-d004437d92a4" />

<img width="621" height="551" alt="Captura de pantalla de 2026-03-30 21-59-15" src="https://github.com/user-attachments/assets/2dc0e928-98af-40f0-a4ce-45b18ba3e9f7" />


### Análisis técnico 

Se pudo comprender como realmente funcionan las redes, los protocolos de diferentes capas involucradas en la comunicación y en sintonia la comprensión del Modelo OSI. Tambien se adquirieron conocimientos adicionales sobre el funcionamiento del apartado Simulación para el analisis y la observación del intercambio de Unidades de Protocolo de Datos de cada protocolo involucrado en la comunicación. 

[Volver al MÓDULO 3](../)
