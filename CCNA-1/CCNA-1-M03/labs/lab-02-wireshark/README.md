# Laboratorio 2 - Capturas de trafico utilizando Wireshark

## Tabla de contenidos

- [Investigación del Modelo OSI](#investigación-del-modelo-osi)
  - [Propósito](#propósito)
  - [Topologia de red](#topologia-de-red)
  - [Procedimientos](#procedimientos)
  - [Análisis técnico](#análisis-técnico)

## Archivos y configuraciones del laboratorio

[CAPTURA DE PAQUETES](../../files/ping-telefono.pcapng)

## Captura de paquetes de protocolo ICMP

### Propósito

Analizar las capturas de paquete al realizar ping a direcciones IP de dispositivos dentro de una red de hogar
### Topologia de Red

- 1 PC
- 1 teléfono celular

### Procedimientos

**Utilización del comando ping desde la PC hacia el teléfono**
  -**Análisis**: Se inicia la aplicación Wireshark y se capturan paquetes que entren o salgan desde la tarjeta de red WLAN de la computadora, por consiguiente, se filtra por paquetes ICMP para observar con mejor claridad. Finalmente desde la terminal de la PC se realiza ping hacia la dirección IP del teléfono, para su posterior análisis por medio de la interfaz de Wireshark donde se analiza el destinatario y receptor de los mismos, tanto como su IP como su dirección MAC. 

<img width="1366" height="768" alt="Captura de pantalla de 2026-04-03 20-02-17" src="https://github.com/user-attachments/assets/e097034c-f0e9-4808-ab94-61997dae2e66" />


[Volver al MÓDULO 3](../)
