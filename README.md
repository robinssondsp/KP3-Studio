# ==========================================================

 _  __ _____ ____      _____ _             _ _
| |/ /|  __ \___ \    / ____| |           | (_)
| ' / | |__) |__) |  | (___ | |_ _   _  __| |_  ___
|  <  |  ___/|__ <    \___ \| __| | | |/ _` | |/ _ \
| . \ | |    ___) |   ____) | |_| |_| | (_| | | (_) |
|_|\_\|_|   |____/   |_____/ \__|\__,_|\__,_|_|\___/

          Windows → YouTube → FL Studio → KP3


# ==========================================================

> Repositorio oficial del estudio de producción basado en **KORG KAOSS PAD KP3**.

---

             _____________________________
            /                            /|
           /____________________________/ |
           |                            | |
           |        WINDOWS AUDIO       | |
           |                            | |
           |   ▶ YouTube  ───────────►  | |
           |                 🍓 FL      | |
           |____________________________|/
                  ||             ||
                  ||             ||
             _____||_____________||_____
            /___________________________\

                💻 Laptop
                     │
                     ▼
             YouTube ─────► FL Studio
                     │
                     ▼
               Voicemeeter
                     │
                     ▼
                KORG KP3
                     │
                     ▼
             Recording / Export
Windows → YouTube → Voicemeeter → FL Studio → KP3 → Recording

> **Versión:** `v1.0`
>
> **Hito del proyecto:** Pipeline de Audio Digital Estable

---

# Descripción General

**KP3 Studio** es un proyecto de investigación y desarrollo orientado a construir un entorno de producción musical híbrido, estable, reproducible y completamente documentado utilizando **Windows**, **Voicemeeter**, **FL Studio** y posteriormente **KORG KAOSS PAD KP3**.

La filosofía del proyecto consiste en documentar cada etapa del desarrollo como una versión independiente, permitiendo reconstruir el estudio completo desde cero en cualquier momento.

La **Versión 1.0** representa el primer hito técnico del proyecto.

El objetivo principal de esta versión no fue integrar hardware externo, sino establecer una infraestructura de audio digital confiable que permita transportar el audio del sistema operativo hasta el Mixer de FL Studio en tiempo real.

Esta arquitectura servirá como base para todas las versiones futuras.

---

# Objetivo de la Versión 1.0

Diseñar, implementar y validar un flujo de audio estable capaz de transportar el sonido generado por aplicaciones de Windows (YouTube) hacia el Mixer de FL Studio utilizando **Voicemeeter Virtual ASIO**.

---

# Arquitectura Implementada

```text
              Audio de Windows
                     │
                     ▼
                  YouTube
                     │
                     ▼
      Voicemeeter Input (VAIO)
                     │
                     ▼
     Voicemeeter Virtual ASIO
                     │
                     ▼
            Mixer de FL Studio
                     │
                     ▼
         Monitoreo en tiempo real
```

---

# Componentes Validados

| Estado | Componente |
|---------|------------|
| ✅ | Configuración de audio de Windows |
| ✅ | Reproducción de YouTube |
| ✅ | Voicemeeter Input |
| ✅ | Salida física Realtek |
| ✅ | Voicemeeter Virtual ASIO |
| ✅ | Comunicación con FL Studio |
| ✅ | Entrada del Mixer |
| ✅ | Monitoreo en tiempo real |
| ✅ | Frecuencia unificada de 48 kHz |

---

# Desafíos Técnicos Superados

Durante el desarrollo de esta versión se resolvieron distintos problemas relacionados con la comunicación entre aplicaciones de audio.

## Conflictos entre Controladores ASIO

Se evaluaron diferentes controladores hasta determinar que **Voicemeeter Virtual ASIO** ofrecía la comunicación más estable entre Windows y FL Studio.

---

## Sincronización de Frecuencia

Se unificó la frecuencia de muestreo de:

- Windows
- Voicemeeter
- FL Studio

estableciendo **48 kHz** como estándar del proyecto y eliminando conflictos de inicialización.

---

## Enrutamiento de Audio

Se configuró Windows para utilizar como dispositivo de reproducción predeterminado:

```
Voicemeeter Input (VB-Audio Voicemeeter VAIO)
```

permitiendo que cualquier aplicación del sistema pueda ser enviada directamente al Mixer de FL Studio.

---

# Arquitectura Final

```text
                 Windows
                    │
                    ▼
                YouTube
                    │
                    ▼
       Voicemeeter Input (VAIO)
                    │
                    ▼
      Voicemeeter Virtual ASIO
                    │
                    ▼
           Mixer de FL Studio
                    │
                    ▼
          Altavoces del portátil
```

---

# Estructura del Proyecto

```text
KP3-Studio/
│
├── backups/
│   ├── kp3/
│   └── voicemeeter/
│
├── docs/
│   ├── 01_Hardware.md
│   ├── 02_Windows.md
│   ├── 03_Voicemeeter.md
│   ├── 04_KP3.md
│   ├── 05_FLStudio.md
│   ├── 06_MIDI.md
│   └── 07_Restore.md
│
├── templates/
│   └── flstudio/
│       └── KP3_Master_Template_v0.1/
│           ├── KP3_Master_Template_v0.1.flp
│           └── Audio/
│
├── CHANGELOG.md
├── README.md
└── .gitignore
```

---

# Alcance de la Versión

La **Versión 1.0** se concentra exclusivamente en la construcción de una infraestructura de transporte de audio digital.

En esta etapa aún no se implementa el procesamiento mediante hardware externo.

Su finalidad es proporcionar una plataforma sólida sobre la cual desarrollar las siguientes versiones del proyecto.

---

# Hoja de Ruta

## ✅ Versión 1.0 — Pipeline de Audio Digital

- Configuración de Windows
- Configuración de Voicemeeter
- Integración con FL Studio
- Monitoreo en tiempo real
- Pipeline de audio estable

---

## 🔄 Versión 2.0 — Integración del KORG KP3

Objetivos previstos:

- Enrutamiento Send / Return
- Procesamiento mediante KP3
- Integración con el Mixer
- Grabación del audio procesado

---

## 🔄 Versión 3.0 — Automatización MIDI

Objetivos previstos:

- Mapeo completo del KP3
- Automatización del XY Pad
- Control MIDI bidireccional
- Plantilla MIDI definitiva

---

## 🔄 Versión 4.0 — Estudio de Producción

Objetivos previstos:

- Plantilla maestra definitiva
- Flujo completo de producción
- Restauración automática
- Documentación integral del estudio

---

# Tecnologías

- Windows
- YouTube
- Voicemeeter
- Voicemeeter Virtual ASIO
- FL Studio
- Git
- GitHub

---

# Estado del Proyecto

## ✅ Hito Técnico Alcanzado

> **La Versión 1.0 establece exitosamente un pipeline de audio digital estable desde aplicaciones de Windows hasta el Mixer de FL Studio.**

Este logro constituye la base técnica sobre la cual se desarrollarán todas las funcionalidades futuras de **KP3 Studio**.