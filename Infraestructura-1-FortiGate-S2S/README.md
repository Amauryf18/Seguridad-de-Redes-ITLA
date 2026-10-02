# Infraestructura 1 - VPN Site-to-Site FortiGate a FortiGate

## 🎥 Video demostrativo

**Ver primero:** [Video demostrativo](video/VIDEO.md)

> Coloca aquí el enlace final de YouTube o OneDrive institucional. El video debe cumplir el máximo de 10 minutos y mostrar fecha/hora, rostro y voz.

## 🎯 Propósito

Comunicar la red de usuarios con la red del servidor mediante un túnel VPN Site-to-Site entre dos FortiGate y comprobar que la comunicación depende de que el túnel VPN esté activo.

## 🗺️ Topología

```mermaid
flowchart LR
    U[Usuarios<br/>VLAN 10<br/>10.3.3.0/24] --> FG1[FortiGate 1<br/>Cliente]
    FG1 --> ISP[ISP / Red pública]
    ISP --> FG2[FortiGate 2<br/>Servidor]
    FG2 --> W[Web Server<br/>192.168.10.0/24]
```

## 📚 Documentación

La documentación completa está en:

- [01 - Introducción](documentacion/01-introduccion.md)
- [02 - Topología y direccionamiento](documentacion/02-topologia-y-direccionamiento.md)
- [03 - Configuración](documentacion/03-configuracion.md)
- [04 - Pruebas y evidencias](documentacion/04-pruebas-y-evidencias.md)
- [05 - Seguridad y conclusiones](documentacion/05-seguridad-y-conclusiones.md)

## 📁 Estructura

```text
.
├── README.md
├── documentacion/
├── imagenes/
├── diagramas/
├── scripts/
├── running-configs/
├── evidencias/
└── video/
```

## 📌 Requisitos de entrega

- Configuración documentada.
- Imágenes.
- Diagrama.
- Propósito del laboratorio.
- Scripts utilizados.
- Running-configs.
- Video demostrativo al principio del repositorio.
- Pruebas que demuestren el objetivo de seguridad.

