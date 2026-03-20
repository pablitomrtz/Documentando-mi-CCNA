# Módulo 1

## Tabla de contenidos

- [Objetivo del módulo](#objetivo-del-módulo)
- [Dispositivos finales](#dispositivos-finales)
- [Dispositivos intermedios](#dispositivos-intermedios)
- [Medios de red](#medios-de-red)
- [Tipos de red](#tipos-de-red)
- [Conexiones a Internet](#conexiones-a-internet)

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

Las conexiones a Internet varían según la ubicación geográfica y la disponibilidad de los ISP.

### Conexiones domésticas

- **Cable**: Se transmiten datos por medio del mismo cable que ofrece televisión por cable.
- **DSL**: Línea de Suscriptor Digital, se transporta por la línea de teléfono. Se utiliza ADSL para oficinas pequeñas. Velocidad de descarga mayor que la de carga.
- **Celular**: Cobertura de telefonía móvil que ofrece acceso a Internet, limitado a las capacidades del teléfono y la torre celular.
- **Satelital**: Ofrecido a quienes no tengan acceso de ninguna otra forma a Internet. Requiere una línea de vista despejada, utilizado en zonas rurales y campos alejados de ciudades.
- **Telefonía Dial-Up**: Opción de bajo costo que proporciona conexión por módem débil. No posibilita la transferencia de datos masivas, útil para acceso móvil en viajes.

<img width="557" height="338" alt="Captura de pantalla de 2026-03-19 21-27-04" src="https://github.com/user-attachments/assets/d3d4eed6-9481-4546-9906-83e3ad0828a5" />

### Conexiones empresariales

Las organizaciones suelen requerir mayor ancho de banda y servidores administrados.

- **Líneas arrendadas dedicadas**: Circuitos reservados dentro del ISP que conectan oficinas remotas para VPNs de voz y/o datos. Las empresas alquilan este servicio mensualmente o anualmente.
- **Metro Ethernet**: Extiende la tecnología LAN a WAN.
- **DSL empresarial**: Utilizado en muchos formatos. El más utilizado es SDSL, con la misma velocidad de subida y descarga.
- **Satelital**: Solución cuando la conexión por cable no es posible.

<img width="559" height="334" alt="Captura de pantalla de 2026-03-19 21-38-50" src="https://github.com/user-attachments/assets/16b69fa3-2ab2-4098-a42c-75349419cdb2" />

## Lab 1 - Representación de una Red en Packet Tracer

Exploración de una topología de red simulada en Packet Tracer con el objetivo de comprender e identificar los componentes principales, la función que cumple cada uno de ellos y analizar la red en su conjunto como red de hogar y empresarial.

<img width="598" height="453" alt="Captura de pantalla de 2026-03-19 22-22-30" src="https://github.com/user-attachments/assets/c699bda3-30d4-47f0-80df-211d229d5057" />

### Análisis de la topología

Durante la exploración de la red se logró identificar una infraestructura empresarial con segmentos interconectados, representando un escenario donde distintas ubicaciones se comunican entre sí en una WAN:

#### Home Office

Representa una red LAN doméstica con PC, Laptop, Tablet, Impresora, Router Inalámbrico y un módem conectado a Internet. El WRS es el punto central, proporciona conexión local y acceso a Internet.

#### Central

Representa una red empresarial más compleja que las demás. Cuenta con un servidor central, routers, switches interconectados y cuatro PCs. Su estructura es más robusta con una gran cantidad de switches para garantizar redundancia, disponibilidad y confiabilidad en la red.

#### Branch

Representa una oficina remota de mayor complejidad que la Home Office. Cuenta con router, switch, PCs, servidor local, impresora, teléfonos IP, smartphone y laptops conectados de forma inalámbrica.

### Dispositivos intermedios

- **Routers**: Se encargan de conectar redes distintas. Ejemplo: LAN to WAN.
- **Switches**: Conectan dispositivos dentro de las redes LAN.

### Medios de red

Cada tipo de medio se selecciona específicamente según la distancia, velocidad y contexto de la red.

- **Cableado Ethernet**: Transmisión por cobre para redes locales de alta velocidad.
- **Cable coaxial**: Transmisión por cobre con blindaje adicional para mayores distancias.
- **Conexión Wireless**: Transmisión inalámbrica para dispositivos móviles.
- **Cableado DTE**: Cables seriales para conexiones entre dispositivos intermedios.

### Análisis conceptual de la red

Los servidores localizados en las redes más complejas (Central y Branch) proporcionan servicios a los dispositivos cliente. Por ejemplo, las PC de Central acceden al servidor central para solicitar información y servicios. El servidor es utilizado principalmente para la transferencia de datos entre los dispositivos de la red.

## Resumen clave

Este módulo establece los fundamentos para comprender cómo funcionan las redes modernas, desde los componentes básicos hasta las topologías complejas. Entender estos conceptos es esencial para el diseño, implementación y mantenimiento de infraestructuras de red en cualquier entorno.

⬅️ [Volver a CCNA 1](../)