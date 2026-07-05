# ==========================================================
#
#      ██╗  ██╗██████╗ ██████╗      ███████╗████████╗██╗   ██╗██████╗ ██╗ ██████╗
#      ██║ ██╔╝██╔══██╗╚════██╗     ██╔════╝╚══██╔══╝██║   ██║██╔══██╗██║██╔═══██╗
#      █████╔╝ ██████╔╝ █████╔╝     ███████╗   ██║   ██║   ██║██║  ██║██║██║   ██║
#      ██╔═██╗ ██╔═══╝  ╚═══██╗     ╚════██║   ██║   ██║   ██║██║  ██║██║██║   ██║
#      ██║  ██╗██║     ██████╔╝     ███████║   ██║   ╚██████╔╝██████╔╝██║╚██████╔╝
#      ╚═╝  ╚═╝╚═╝     ╚═════╝      ╚══════╝   ╚═╝    ╚═════╝ ╚═════╝ ╚═╝ ╚═════╝
#
# ==========================================================

# KP3-Studio

> Repositorio oficial del estudio de producción basado en **KORG KAOSS PAD KP3**.

---

## Objetivo

Este repositorio almacena toda la infraestructura necesaria para reconstruir completamente mi estudio de producción en cualquier computadora.

Incluye:

- Configuración de Windows
- Configuración de Voicemeeter
- Plantillas de FL Studio
- Mapeos MIDI
- Backups del KP3
- Documentación técnica
- Scripts
- Historial de cambios

---

## Estado actual

| Estado | Componente |
|---------|------------|
| ✅ | Driver KORG USB MIDI instalado |
| ✅ | Windows detecta el KP3 |
| ✅ | KP3 Editor comunica correctamente |
| ✅ | RECEIVE verificado |
| ✅ | FL Studio detecta el KP3 |
| ✅ | Voicemeeter funcionando |
| ✅ | Audio HDMI funcionando |

---

## Arquitectura del estudio

```text
                    +--------------------+
                    |     YouTube        |
                    +---------+----------+
                              |
                              v
                 +--------------------------+
                 |      Voicemeeter         |
                 +-----------+--------------+
                             |
               +-------------+-------------+
               |                           |
               v                           v
      +----------------+          +------------------+
      |   FL Studio    |          |  HDMI Monitor    |
      +-------+--------+          +------------------+
              |
              |
              v
      +----------------+
      |    KORG KP3    |
      +----------------+
```

---

## Estructura del proyecto

```text
KP3-Studio
│
├── backups
│   ├── flstudio
│   ├── kp3
│   └── voicemeeter
│
├── docs
│
├── exports
│
├── midi
│   ├── mapping
│   └── presets
│
├── scripts
│
├── screenshots
│
├── templates
│   ├── flstudio
│   └── mixer
│
├── tools
│   ├── korg
│   └── vb-audio
│
├── CHANGELOG.md
├── README.md
└── .gitignore
```

---

## Objetivos del proyecto

- Crear un estudio completamente reproducible.
- Versionar todas las configuraciones.
- Automatizar los respaldos.
- Automatizar la restauración.
- Mantener documentación técnica.
- Centralizar todos los recursos del KP3.

---

## Roadmap

### Fase 1
- [x] Instalación de Drivers
- [x] KP3 reconocido por Windows
- [x] KP3 Editor funcionando
- [x] Voicemeeter configurado

### Fase 2
- [ ] Plantilla maestra de FL Studio
- [ ] Mapeo MIDI completo
- [ ] Automatización del XY Pad
- [ ] Configuración del Mixer

### Fase 3

- [ ] Scripts automáticos
- [ ] Restauración automática
- [ ] Backup de configuración
- [ ] Manual completo

---

## Tecnologías

- KORG KAOSS PAD KP3
- FL Studio
- Voicemeeter
- VB Audio Cable
- Windows
- Git
- GitHub

---

## Historial

Consulta:

```
CHANGELOG.md
```

---

## Autor

**Robinsson De Sousa Pérez**

Uruguay

2026