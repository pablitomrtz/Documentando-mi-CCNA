# Módulo 1

## Tabla de contenidos

- [Objetivo del módulo](#objetivo-del-módulo)
- [Dispositivos finales](#dispositivos-finales)
- [Dispositivos intermedios](#dispositivos-intermedios)
- [Medios de red](#medios-de-red)
- [Tipos de red](#tipos-de-red)

## Objetivo del módulo

Comprender qué es una red, cómo interactúan los dispositivos dentro de ella, cómo funcionan los mecanismos que permiten esta interacción y por qué son fundamentales en la actualidad, ya sea en entornos domésticos o empresariales.

## Dispositivos finales

Dentro de la red, encontramos quiénes la forman: dispositivos interconectados que se comunican entre sí para compartir información y recursos.

- **Hosts**: Cualquier dispositivo de la red que posee una dirección **IP** y puede enviar o recibir información.
- **Servidor**: Computadoras con software que permite proporcionar información (ejemplo: correo o sitios web) a otros hosts dentro de la red. Para cada información específica requiere un software de servidor independiente.
- **Cliente**: Se refiere específicamente a los dispositivos finales que poseen software para solicitar y mostrar información obtenida del servidor (ejemplo: Google Chrome, Brave).

## Dispositivos intermedios

Son los encargados de conectar los dispositivos finales y permitir la comunicación entre ellos. Utilizan información como direcciones **IP** y tablas de enrutamiento para determinar la ruta más eficiente para transmitir los datos dentro de la red.

- **Routers**: Dispositivos que dirigen el tráfico de datos entre redes.
- **Switches**: Conectan dispositivos dentro de una misma red local (LAN).
- **Firewalls**: Proporcionan seguridad filtrando el tráfico de red.

## Medios de red

Proporciona el canal por el cual se envía el mensaje desde el origen al destino. Existen tres tipos de medios principales:

- **Cobre**: Transmisión de datos mediante pulsos eléctricos.
- **Fibra óptica**: Codificación de datos a través de pulsos de luz.
- **Tecnología inalámbrica**: Modulación de frecuencias específicas de ondas electromagnéticas para la codificación de los datos.

![Captura de pantalla de 2026-03-18 17-46-11](https://github.com/user-attachments/assets/7de7a13c-ac7b-41d3-aca6-4bcd50e2f6d6)

## Tipos de red

- **Redes LAN**: Infraestructura de la red que abarca un área geográfica pequeña. Interconecta un área limitada (ejemplos: una casa, un edificio de oficinas o un campus).
- **Redes WAN**: Infraestructura que abarca un área geográfica extensa, administrada generalmente por **ISP**. Interconectan LANs en áreas geográficas más extensas (ejemplos: ciudades, provincias, países o continentes).
- **Internet**: Llamada *internetworks*, es la colección global de redes interconectadas.
- **Extranet**: Redes de empresas que otorgan acceso protegido a usuarios de otras organizaciones que deseen acceder a sus datos (ejemplo: una empresa que proporciona acceso a proveedores y contratistas externos).
- **Intranet**: Conexión privada dentro de una organización, diseñada para el acceso exclusivo de empleados y miembros de la organización.

## Conexiones a Internet

Varian segun ubicacion geografica y la disponibilidad de los ISP.

Conexiones domesticas

- Cable: se transmiten datos por medio del mismo cable que ofrece television por cable
- DSL: Linea de Suscriptor Digital, se transporta por la linea de telefono, se utiliza ADSL para oficinas pequeñas. Velocidad de descarga mayor que la de carga
- Celular: cobertura de telefonia movil que ofrece acceso a internet, limitado a las capacidades del telefono y la torre celular.
- Satelital: ofrecido a quienes no tengan acceso de ninguna otra forma a internet, requiere una linea de vista despejada, utilizado en zonas rurales, campos alejados de ciudades, etc.
- Telefonia Dial-Up: opcion de bajo costo, proporciona conexion por modem debil, no posibilita la transferencia de datos masivas, util para acceso movil en viajes.

<img width="557" height="338" alt="Captura de pantalla de 2026-03-19 21-27-04" src="https://github.com/user-attachments/assets/d3d4eed6-9481-4546-9906-83e3ad0828a5" />

Conexiones Empresariales

Las organizaciones suelen requerir mayor ancho de banda y servidores administrados 
- Lineas arrendadas dedicadas: circuitos reservados dentro del ISP que conectan oficinas remotas para VPNs de voz y/o datos. Empresas alquilan este servicio mensual o anualmente.
- Metro Ethernet: extiende la tecnologia LAN a WAN
- DSL empresarial: utilizado en muchos formatos, el mas utilizado SDLS, misma velocidad de subida y descarga
- Satelital: solucion cuando la conexion por cable no es posible

<img width="559" height="334" alt="Captura de pantalla de 2026-03-19 21-38-50" src="https://github.com/user-attachments/assets/16b69fa3-2ab2-4098-a42c-75349419cdb2" />

## Lab 1 - Representacion de una Red en Packet Tracer

Exploracion de una topologia de red simulada en Packet Tracer con el objetivo de comprender e identificar componentes principales, la funcion que cumple cada uno de ellos y analizar la red en su conjunto como red de hogar y empresarial.

<img width="598" height="453" alt="Captura de pantalla de 2026-03-19 22-22-30" src="https://github.com/user-attachments/assets/c699bda3-30d4-47f0-80df-211d229d5057" />


Analisis de la topologia

Durante la exploracion de la red se logro identificar una infraestructura empresarial con segmentos interconectados, representando un escenario donde distintas ubicaciones se comunican entre si en una WAN:
- Home Office
- Central
- Branch
- Conexion por Internet e Intranet

Home Office

Representando una red LAN domestica con PC, Laptop, Tablet, Impresora, Router Inalambrico y un modem conectado a internet. El WRS es el punto central, proporciona conexion local y acceso a internet.

Central

Representa una red empresarial mas compleja que las demas, cuenta con un servidor central, routers, switches interconectados y cuatro PCs. Su estructura es mas robusta gran cantidad de switches, para garantizar redundancia, disponibilidad y confiabilidad a la red.

Branch

Representa una oficina remota de mayor complejidad que la Home Office, cuenta con router, switch, PCs, Servidor local, impresora, telefonos IP, Smartphone y Laptops conectados de forma inalambrica.

Dispositivos intermedios

- Routers: se encargan de conectar redes distintas, Ej LAN to WAN.
- Switches: conectan dispositivos dentro de las redes LAN

Medios de red

Cada tipo de medio se selecciona especificamente segun distancia, velocidad y contexto de la red.

- Cableado Ethernet
- Cable coaxial
- Conexion Wireless
- Cableado DTE

 Analisis conceptual de la red
 Los servidores localizados en las redes mas complejas, Central y Branch, proporcionan servicios a los dispositivos cliente. Ejemplo, las PC de Central acceden al servidor central para solicitar informacion y servicios, especificamente para lo que el servidor es utilizado es en transferencia de datos entre los dispositivos de la red.
 
⬅️ [Volver a CCNA 1](../)
