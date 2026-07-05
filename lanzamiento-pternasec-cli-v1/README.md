---
title: "Lanzamiento Oficial: PternaSec CLI v1.0.0"
description: "Anunciamos la disponibilidad global del nuevo PternaSec CLI. Una potente herramienta interactiva para automatizar auditorías, descargar herramientas OSINT y ejecutar contenedores."
category: "actualizacion"
date: "2026-07-05T12:00:00Z"
read_time: "4 min"
---

# El Motor de Ciberseguridad Definitivo ya está aquí

Nos emociona anunciar el lanzamiento oficial de **PternaSec CLI v1.0.0**, el corazón de nuestro ecosistema. Diseñado meticulosamente para analistas de ciberseguridad, pentesters e investigadores OSINT, esta nueva herramienta resuelve uno de los mayores problemas de la industria: la gestión fragmentada de herramientas.

## ¿Qué puedes hacer con PternaSec CLI?

El CLI transforma tu terminal en una estación de mando centralizada e interactiva. 

* **Navegación TUI (Terminal User Interface):** Olvídate de memorizar largos comandos. Navega por categorías como OSINT, Red-Team y Blue-Team usando menús dinámicos e intuitivos.
* **Búsqueda Global:** Encuentra la herramienta exacta que necesitas al instante.
* **Descarga y Ejecución Inteligente:** Ya no necesitas lidiar con `git clone` y resolver dependencias rotas a mano. El CLI detecta si una herramienta usa Python, Bash o Node, y la ejecuta en un entorno seguro por ti.

## Disponibilidad Inmediata

Como parte de nuestro compromiso con el software de código abierto y la accesibilidad, hemos publicado el CLI en dos de los registros más importantes del mundo.

### 1. NPM (Para entusiastas de Node.js)
Puedes instalarlo globalmente en cualquier sistema con Node.js ejecutando:
```bash
npm install -g pternasec-cli
```

### 2. Docker (Para entornos aislados y DevSecOps)
Si prefieres mantener tu máquina inmaculada o integrarlo en pipelines automatizados, hemos publicado el contenedor oficial en el *GitHub Container Registry*:
```bash
docker run -it --rm \
  -v ~/.pternasec/scripts:/root/.pternasec/scripts \
  ghcr.io/pternasec/cli-core:latest
```

Estamos ansiosos por ver cómo la comunidad de ciberseguridad integra esta nueva CLI en sus operaciones diarias. ¡Mantén tus sistemas seguros!
