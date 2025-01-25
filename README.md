# Servicio de Video GreyCloud, empresa ficticia


#### Llevado a cabo por: Diego Orrillo (https://github.com/Diego0rrill0)

## Tabla de Contenidos

- [Introducción](#introducción)
- [Características](#características)
- [Configuración del Servidor](#configuración-del-servidor)
- [Pruebas](#pruebas)
- [Herramientas de Videoconferencias](#herramientas-de-videoconferencias)
- [Guía de Instalación](#guía-de-instalación)
- [Conclusiones](#conclusiones)

## Introducción

GreyCloud, una empresa especializada en ciberseguridad y distribución de software, ha desarrollado un servicio de video diseñado para satisfacer las necesidades de su equipo interno, clientes empresariales y audiencia externa. Este proyecto incluye la configuración de un servidor de video con Nginx y una página web básica que organiza los videos en categorías accesibles solo mediante autenticación.

## Características

- **Streaming y descarga de videos**.
- **Autenticación básica** para proteger los contenidos.
- **Categorías organizadas por perfiles de usuario:**
  - **Equipo Interno:** Contenido formativo y actualizaciones internas.
  - **Clientes Empresariales:** Material sobre productos, casos de estudio y soluciones.
  - **Audiencia Externa:** Videos educativos, promociones y charlas del sector.
- **Compatibilidad con múltiples formatos:** MP4, AVI, WEBM, HEVC.

## Configuración del Servidor

1. **Instalación y configuración de Nginx:**
   - Ruta principal: `/home/diego/nginx/conf/nginx.conf`.
   - Protección con autenticación básica mediante `apache2-utils`.
2. **Permisos:**
   - Configuración de permisos y propietarios para carpetas y archivos con `chmod` y `chown`.
3. **Categorías de usuarios y credenciales:**
   - `Equipointerno` (Contraseña: `12345`)
   - `Clientesempresariales` (Contraseña: `123456`)
   - `Audienciaexterna` (Contraseña: `1234567`)

## Pruebas

- **Conexión al servidor:**
  - Prueba de acceso mediante credenciales.
  - Reproducción y descarga de videos a través de enlaces clickeables.
- **Prueba de autenticación:**
  - Credenciales solicitadas al ingresar a las categorías.
- **Verificación de configuración:**
  - Comandos utilizados:
    ```bash
    /home/diego/nginx/sbin/nginx -t
    /home/diego/nginx/sbin/nginx -s reload
    ```

## Herramientas de Videoconferencias

Se evaluaron y configuraron herramientas como **Zoom** y **Microsoft Teams** para complementar el servicio de video:

- **Protocolos y características implementados:**
  - Seguridad (SRTP y TLS).
  - Interoperabilidad entre plataformas.
  - Grabación de reuniones.
  - Compatibilidad con dispositivos y sistemas operativos.

## Guía de Instalación

### Instalación de Zoom en Ubuntu Desktop
1. **Actualizar repositorios:**
sudo apt update
wget https://zoom.us/client/latest/zoom_amd64.deb
sudo apt install ./zoom_amd64.deb
2. **Ejecución de zoom**
Sólo debemos escribir zoom en el bash

## Conclusiones
El servicio de video y las herramientas de videoconferencia implementadas permiten a GreyCloud mejorar la comunicación y capacitación de su equipo, al mismo tiempo que fortalecen su relación con clientes y audiencia externa. La configuración es segura, eficiente y escalable, adaptable para futuros requerimientos.
