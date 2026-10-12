# Integrated-Project
# Plataforma Empresarial Distribuida: Sistema de Gestión de Correos

Este repositorio contiene el código fuente, los servicios de autenticación y la documentación de la infraestructura de red.

## Arquitectura del Proyecto

El proyecto implementa una solución tecnológica distribuida entre dos sedes (Sede A y Sede B), integrando desarrollo de software, seguridad e infraestructura de comunicaciones:
*   **App-Go:** Servidor backend desarrollado en Go para la gestión de mensajería y correos internos.
*   **Auth-Service:** API REST desarrollada en FastAPI (Python) para la emisión y validación de tokens de acceso seguro.
*   **Network:** Infraestructura de red segmentada mediante VLANs, enrutamiento OSPFv2, Router-on-a-Stick con OpenWrt y switches Cisco, conectando ambas sedes a través de un enlace inalámbrico.

## Estructura del Repositorio

*   `/app-go`: Código fuente del sistema de correos (backend).
*   `/auth-service`: Servicio de autenticación y gestión de credenciales.
*   `/network`: Entregables de red, diagramas lógicos/físicos, tablas VLSM y respaldos de configuración de Cisco/OpenWrt.
*   `/docs`: Documentación académica, informes de planificación y análisis estadístico.

## Requisitos de Ejecución

*   **Software:** Go 1.20+, Python 3.10+, Cisco Packet Tracer.
*   **Infraestructura:** Imágenes de OpenWrt x86, switches Cisco (LACP/PAgP, RSTP).
*   **Despliegue:** WSL (Windows Subsystem for Linux) o entorno Linux nativo.

## Autores y Responsabilidades

*   **Juan Andrés Pesantez:** Integración de la aplicación Go/FastAPI, reglas de firewall, pruebas finales de enrutamiento, documentación y gestión del repositorio Git.
*   **Ariel Yumbillo:** Configuraciones de Capa 2 (VLAN, enlaces troncales 802.1Q, EtherChannel, RSTP), reglas de firewall, pruebas finales de enrutamiento y documentación.
*   **Israel Farfán:**  Integration of the Go/FastAPI application, firewall rules, and final routing tests, Layer 3 edge implementation (OpenWrt, OSPF, DHCP, NAT).

## Licencia
El proyecto se distribuye bajo la licencia MIT. 