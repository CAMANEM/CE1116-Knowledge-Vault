---
Fecha de creación: 2026-04-29 19:49
Fecha de Modificación: 2026-04-29 21:00
tags:
  - Conceptos
Tema: Cloud
---
# ☁️ Cloud Computing — Conceptos Clave

> [!info] Sobre estas notas Conceptos fundamentales de computación en la nube: modelos de servicio, tipos de despliegue, escalamiento y redundancia.

---

## 🌐 Modelos de Despliegue

### Cloud Público

> [!quote] Mi definición

> Modelo de servicios de computación en el que se paga según lo que se consume. Los datos siguen siendo privados según se requiera.

- Modelo de pago por consumo (_pay-as-you-go_)
- Los datos siguen siendo privados según se requiera
- Infraestructura compartida administrada por el proveedor

### Virtual Private Cloud (VPC)

> [!quote] Mi definición

> Servicio de red virtual aislada que otorga control total sobre subredes, tablas de ruteo y firewalls, operando como una sección privada dentro de la nube pública. Su red puede incluso ser invisible para dispositivos que comparten mismo hardware.

- Red virtual **aislada** dentro de la nube pública
- Otorga control total sobre:
    - Subredes
    - Tablas de ruteo
    - Firewalls
- La red puede ser **invisible** para otros dispositivos que comparten el mismo hardware

### Cloud Híbrido _(Hybrid Cloud)_

> [!quote] Mi definición

> Modelo de servicios que mezcla características de cloud pública y privada, lo cual brinda versatilidad y escalabilidad en aplicaciones.

- Mezcla características de cloud pública y privada
- Brinda **versatilidad** y **escalabilidad** en aplicaciones
- Ideal para organizaciones con requisitos mixtos

---

## ⚖️ Modelos de Servicio — IaaS vs PaaS vs SaaS

> [!quote] Mi definición

> **IaaS:** el proveedor facilita el equipo con los recursos deseados y el cliente se encarga de la configuración. **PaaS:** el proveedor brinda el servidor con los recursos y configuraciones deseadas, listo para nada más subir y correr la aplicación deseada. **SaaS:** el proveedor provee servidor, configuración y hasta la aplicación lista ya para usar a los usuarios (ej: Youtube, Netflix).

|Modelo|Nombre completo|¿Qué provee el proveedor?|¿Qué hace el cliente?|
|---|---|---|---|
|**IaaS**|Infrastructure as a Service|Equipo y recursos físicos/virtuales|Configuración completa|
|**PaaS**|Platform as a Service|Servidor + recursos + configuración|Solo subir y correr la aplicación|
|**SaaS**|Software as a Service|Servidor + configuración + aplicación lista|Solo usar|

> [!example] Ejemplos de SaaS YouTube, Netflix, Google Docs, Spotify

---

## 📈 Escalamiento en el Cloud

### Escalamiento Vertical _(Scale Up)_

> [!quote] Mi definición

> Consiste en incrementar recursos como CPU y RAM.

- Agregar más CPU
- Aumentar RAM
- Mayor capacidad de almacenamiento

### Escalamiento Horizontal _(Scale Out)_

> [!quote] Mi definición

> Consiste en agregar más servidores para distribuir la carga de trabajo.

- Se añaden más nodos al sistema
- Mejor tolerancia a fallos
- Preferido para aplicaciones de alta disponibilidad

```
Vertical:   [Servidor  ↑↑]
Horizontal: [Servidor] + [Servidor] + [Servidor]
```

---

## 🛡️ Redundancia en el Cloud

La redundancia garantiza disponibilidad de datos ante fallos.

### 🏢 Redundancia Local

> [!quote] Mi definición

> Las copias de seguridad de su información se encuentran en el mismo cluster o centro físico de datos. Si un disco falla, se tiene una copia cerca, físicamente.

- Las copias de seguridad están en el **mismo clúster o centro de datos físico**
- Si un disco falla → copia disponible de manera cercana, físicamente
- Protege contra: fallos de disco individuales

### 🏙️ Redundancia por Zona

> [!quote] Mi definición

> Las copias de seguridad se encuentran en un lugar distinto por lo que incluso si sucede una falla a nivel de edificio, se cuenta con un respaldo en otro lugar.

- Las copias están en un **lugar físico distinto**
- Si falla un edificio completo → respaldo en otra ubicación
- Protege contra: fallos a nivel de edificio o zona

### 🌍 Geo-Redundancia _(Geo-Redundant)_

> [!quote] Mi definición

> Las copias de seguridad se encuentran en otra región del planeta por lo que incluso si toda una región falla, se cuenta con otra copia en alguna parte del mundo.

- Las copias se encuentran en **otra región del planeta**
- Si falla toda una región → copia disponible en otra parte del mundo
- Protege contra: desastres regionales, fallos masivos de infraestructura

> [!tip] Regla general de redundancia A mayor distribución geográfica → mayor resiliencia, pero también mayor latencia y costo.

---

## 🗺️ Mapa de Conceptos

```
Cloud Computing
├── Modelos de Despliegue
│   ├── Cloud Público
│   ├── VPC
│   └── Cloud Híbrido
├── Modelos de Servicio
│   ├── IaaS
│   ├── PaaS
│   └── SaaS
├── Escalamiento
│   ├── Vertical (más recursos)
│   └── Horizontal (más servidores)
└── Redundancia
    ├── Local (mismo cluster)
    ├── Por Zona (otro edificio)
    └── Geo-Redundante (otra región)
```

---

## 🏷️ Tags

`#cloud` `#infraestructura` `#IaaS` `#PaaS` `#SaaS` `#escalamiento` `#redundancia` `#VPC` `#arquitectura`